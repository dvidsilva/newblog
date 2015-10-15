---
layout: post
title: "What to check before making your site live"
description: "Answer for a friend that has had issues finding what to look for before publishing changes on your site."
tagline: ""
categories : [web-development]
tags: [Web Development, CMS]
---
{% include JB/setup %}

A friend asked me recently what steps do I usually take at work before we publish our website. Our company is not a website,
so we are more lenient on it than we are with our product, specially the server code; we don't run automated tests in our 
website, but we have a checklist of things that we go through before publishing changes.

It looks like this:

1. See what new blog posts where created or what was edited recently, most CMS have the option to sort posts by last edited
or created to make this easier.

2. Look at the content and make sure the images look fine, and content is as it should be, including:
 * make sure meta tags and description are correct 
 * if there are links on the content, click on them and make sure they work
 * if there are forms, test them with several input, and errors, and make sure they work

3. Look at outstanding tickets and see if they were resovled

4. Make sure things that should be private or internal are that way

5. Bring visibility into the process by having a coworker or two also approve the changes before they go live.
(This also lets you have someone you can share the blame with if things go wrong)


### Notes

* If new plugins were installed, a new version of the CMS was downloaded, or big changes were made, the check should 
be a lot stricter.

* We don't check for technical things, like if the database is running, we assume they are; for uptime and
performance you can use monitoring software like [NewRelic](http://newrelic.com/).

* Check on several devices and browsers, at least one smartphone a tabled chrome and safari. 
When redesigning or implementing big changes add IE, Edge, and different versions of operative systems.


