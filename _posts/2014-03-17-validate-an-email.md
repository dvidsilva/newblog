---
layout: post
title: "validate an email"
description: "The regular expression that validates e-mails according to the RFC standard, explained."
category: Programming
tags: [regexp]
---
{% include JB/setup %}


So I recently found out about this [website](http://regex101.com/#javascript) where you can try out regular expressions, either to practice or test them before sending them live. 

Really useful, the coolest feature it has tho, is that it explains step by step what the expression is doing, so a friend decided to see what would happen with one of the hardest, regexp that
we end up writing every now and then, emails.


E-mail validator Regexp
============

I used the regexp described [here](http://forums.asp.net/t/1132908.aspx?How+to+validate+Email+as+per+RFC+2822+standards).




{% highlight javascript %}
(?:[a-z0-9!#$%&'*+/=?^_`{|}~-]+(?:\.[a-z0-9!#$%&'*+/=?^_`{|}~-]+)*|"(?:[\x01-\x08\x0b\x0c\x0e-\x1f\x21\x23-\x5b\x5d-\x7f]|\\[\x01-\x09\x0b\x0c\x0e-\x7f])*")@(?:(?:[a-z0-9](?:[a-z0-9-]*[a-z0-9])?\.)+[a-z0-9](?:[a-z0-9-]*[a-z0-9])?|\[(?:(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.){3}(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?|[a-z0-9-]*[a-z0-9]:(?:[\x01-\x08\x0b\x0c\x0e-\x1f\x21-\x5a\x53-\x7f]|\\[\x01-\x09\x0b\x0c\x0e-\x7f])+)\])
{% endhighlight %}


I tried including their explanation below, but better go ahead and try it in [their site](http://regex101.com/r/xF4jF3), stupid markdown :P


