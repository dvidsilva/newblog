---
layout: post
title: "Fetching JSON from an URI to your database."
description: "How to use HTTParty and JSON to read JSON from a external resource and add it to your database."
tagline: ""
categories : [programming]
tags: [rails,programming,apis, hackership]
---
{% include JB/setup %}

For part of your projects, and possible for many things you work on it will be important to get information from external servers, either to complement the information on your database or to populate your database with information from different providers. This process is called scrapping, in this exercise we will use a site that returns JSON responses, so is easier to work with, a more advanced scrapping process can involve API authorizations or parsing HTML to read the content.

The result can be found here, in case you are stuck with syntax, but try to follow along, it should be a short exercise.
https://github.com/hackershipco/scrapy

The code in the blog seems to be formatted unproperly, for a better version see it on [github](https://github.com/dvidsilva/blog/blob/gh-pages/_posts/2014-11-07-fetching-json-from-url.md), 

We are going to get the information that results from this URL http://omdbapi.com/?t=vicky+cristina and add it to our database.

Preparing
---

Create a new rails app in your desktop or projects folder, we can call it scrapy.

```
rails new scrapy
```

Add two gems to your gemfile:

```
gem 'httparty'
gem 'json'
```

HTTParty makes creating web requests easier, we're using it to GET information in this case, but it can be use to simulate POST or any other kind of requests. More about it [here](https://github.com/jnunemaker/httparty).

The JSON gem allows to manipulate/convert data to and from JSON. You can read more about it [in their project's page](https://github.com/flori/json).

Model and Controller
---

Lets create a controller that will have the action we can use to fetch the information and the Model where we will store the results.

For the model we're creating a Movie with the following fields by running:

```
rails g model movie title:string director:string year:integer plot:string oscars:integer
```

For the controller we want a scraper controller with a scrap action.
```
rails g controller scraper scrap
```
*In the source code that's on GitHub the controller is called ScrapperController, this is a typo. You can name it any way you want*. 
You could also add the action to  one of your existing controllers and create a route.

Lets modify that action so something happens. 

```
  def scrap
    url = "http://omdbapi.com/?t=" + params[:movie]
   render text: url
  end
```
Now if you go to  http://localhost:3000/scrapper/scrap?movie=inception the browser should output a text with the url.

Scraping
---

I'm gonna be adding little by little to the controller, always replace or rewrite the scrap action, I want to walk you through the different steps one by one, so you can replace your action and go to the browser and see the difference.

**Fetching JSON**

```
  def scrap
    url = "http://omdbapi.com/?t=" + params[:movie]
    @response = HTTParty.get(URI.encode(url))
    @result = JSON.parse(@response.body)
   render json: @result
  end
```

http://localhost:3000/scrapper/scrap?movie=inception

**Verifying that the information works.** This is a good debugging method, replace your render for `render json: @result` with a variable you want to see what contains, that way you can also inspect which properties are returned and how to access them.

```
  def scrap
    url = "http://omdbapi.com/?t=" + params[:movie]
    @response = HTTParty.get(URI.encode(url))
    @result = JSON.parse(@response.body)
   if @result["Title"] == nil
      render json: {:error => "COULDNT FIND THAT MOVIE :( "}.to_json
   else
     render json: @result
   end
  end
```
http://localhost:3000/scrapper/scrap?movie=life+is+cool+2

**Saving in the database**
```
class ScrapperController < ApplicationController
  def scrap
    url = "http://omdbapi.com/?t=" + params[:movie]

    @response = HTTParty.get(URI.encode(url))
    @result = JSON.parse(@response.body)

    @movie = Movie.new
    if @result["Title"] == nil
      return render json: {:error => "COULDNT FIND THAT MOVIE :( "}.to_json
    end
    # checking if the movie exists already #
    if( Movie.exists?(title: @result["Title"]) and Movie.exists?(year: @result["Year"] ))
      @movie = Movie.where("title = ?", @result["Title"]).first
    end
    # saving the properties of the JSON response into the movie instance
    @movie.title = @result["Title"]
    @movie.director = @result["Director"]
    @movie.year = @result["Year"]
    @movie.plot = @result["Plot"]
    # the JSON response brings the awards as:
    # Won 1 Oscar. Another 32 wins & 38 nominations
    # we are using regular expressions to get the number of oscars from that string
    oscars = @result["Awards"].match(/(?<number>[\d]+)\s+(o|Oscar)/)
    @movie.oscars = (( oscars == nil || oscars["number"] == nil) ? 0 : oscars["number"])

    if @movie.save
      render json: @movie
    else
      render json: {:error => "MEGAFAIL!"}.to_json
    end
  end
end
```

http://localhost:3000/scrapper/scrap?movie=inception

[Regular Expressions Introduction](http://www.ruby-doc.org/core-2.1.1/Regexp.html)

Hope this helps in your projects, add specific questions to your implementation let me know.


In the case of Reddit just append `.json` to any url https://www.reddit.com/r/tumblrinaction.json

