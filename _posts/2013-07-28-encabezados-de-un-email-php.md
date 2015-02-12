---
layout: post
title: "encabezados de un email php"
description: ""
category: 
tags: []
---
{% include JB/setup %}
There have been many questions raised by our members on how email clients set the Content-Type within their HTML emails. As you may already know, the Content-Type plays a major role in the way an email will be displayed, especially with respect to special characters in non-Latin languages or when copying from a text editor like Microsoft Word.
In summary, all email clients ignore the Content-Type defined within your meta tag. Instead, they read it from the Content-Type value that is in the header of your email. The character type value within the header is automatically set by the server sending your email. This value can be changed but you would need direct access to the email server. The safest solution is to convert all of your special characters to HTML entities and we have created a free online tool to help assist you in that process.
What is Content-Type?
A Content-Type tells the web browser or email application how to interpret the text characters in your HTML or the body of the email. The most popular character sets are UTF-8 and ISO-8859-1.
To illustrate, let's take the following code:
<p>UTF-8 Characters: ö ü ä</p>
<p>UTF-8 Chinese: æ¿€ å…‰ é€™ </p>
<p>HTML Entity Characters: &#28450; &#23383;</p>
Here's how it renders using each character set:

As you can see above, the Chinese symbols are not represented in the ISO-8859-1 character set. This is because ISO-8859-1 only includes Latin based language characters. The result is a bunch of jumbled text, which is the ISO-8859-1 interpretation of the symbols.
Where does this all fit into HTML emails?
In website development, we can tell the web browser what character set to use in a meta tag like this:
<meta http-equiv="Content-Type" content="text/html charset=UTF-8" />
Emails are displayed in clients using the same premise. It will display the email based on what Content-Type has been set. However, email clients read the Content-Type value that is set in the email header and they completely ignore the META tag that is within the HTML.
How does the email header Content-Type get set?
The header content is set by the server sending the email and contains information like To, From, Date, Time, etc. Some of which is displayed at the top of each email when viewing it in an email client.
Here is a snippet of an email header (notice the Content-Type value):
Date: Wed, 15 Dec 2010 12:45:55 -0700
To: test@test.com
From: testfrom@test.com
Subject: UTF-8
Message-ID: <e06deabc923f3378e4b237a20be324cc@www.test.com>
X-Priority: 3
X-Mailer: EOAMailer 5.0.0
MIME-Version: 1.0
Content-Transfer-Encoding: 8bit
Content-Type: text/html; charset="UTF-8"
Email client test results
I sent the above code example to all the email clients that we support. Pretty much every client renders text based on the Content-Type value set in the email header. Gmail is the only client that automatically converts your text to UTF-8, no matter what the header Content-Type is set to.
Here are the test results:
ClientsContent-Type
AOL
Hotmail
Outlook Express 
Outlook 2003, 2007 and 2010
Lotus Notes 6.5, 7, 8 and 8.5
Live Mail
Windows Mail
Entourage 04 and 08
Yahoo Classic, Current, and Beta
Thunderbird 2 and 3
iPad
iPhone Mail
Android MailEach take the Content-Type from th  e header of your email
Gmail
Android Gmail
iPhone Gmail
iPad GmailEach   convert the Content-Type to UTF-8

One thing that I found very suprising is the fact that the web-based clients convert your text to the Content-Type character set prior to displaying it in the browser. I was able to check this by viewing what Content-Type they were setting in their META tags. As it turns out most of them are using UTF-8.
The Solution
Now you might be saying to yourself, great just when I thought designing emails wasn't complicated enough. It does in-fact add another layer of complexity but there are a couple fairly easy solutions.
Option 1:
Contact your email service provider and ask them what Content-Type they set in the header when sending the emails. Once you know the Content-Type use that value in your HTML Meta tag when designing the email.
Option 2:
Convert all special characters to their HTML entities and you won't have to worry about the header Content-Type. For example, the following character "æ¼¢" has an HTML entity value of "&#28450;". To help assist you in the conversion we have created a free online tool that will convert all of your special characters for you! Just use this conversion tool before you send your email.
In Conclusion
It is always important to check your character sets using both IE and Firefox, especially if you are using non-Latin characters or copy/pasting content from a text editor like Microsoft Word.
At this time, when you submit an Acid Test, our servers are configured to send your email using the UTF-8 Content-Type to each of our supported email clients.  We will be adding an option for selecting your Content-Type in the near future.

