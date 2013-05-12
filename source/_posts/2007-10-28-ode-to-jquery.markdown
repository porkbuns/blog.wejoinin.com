---
author: DarkWulf
comments: true
date: 2007-10-28 16:59:25
layout: post
slug: ode-to-jquery
title: Ode to jQuery
wordpress_id: 16
categories:
- Development
---

I guess Andrew goaded me into posting. I always think of him as the friendly face of Wejoinin, whereas I am the (code) ninja who merely leaves destruction (and lines of code) in his wake.

The move to jQuery was largely started when I one day looked at the Wejoinin signup sheet page and went "holy cow? 150kilobytes of javascript?! what are we doing here?!" I mean, [Prototype](http://www.prototypejs.org/) has a few chins now (and quite an expansive belly), and ditto for Scriptaculous and whatever else that we were using, but 150KB?! There was then a protracted session of slow consideration of different Javascript libraries considering their APIs, their filesize, their compatibi- haha, no I just chose one out of a hat. I chose [jQuery](http://jquery.com/).

(Sidenote: I totally went to a talk by John Resig (author of jQuery), and it was totally rad.)

Andrew is looking at me and pointing at his watch. I think I've been rambling? Oh where was I?

Right, moving to jQuery turned our 150KB monstrosity of Javascript to a much more sane 40KB or so. The HTML we sent thinned down a bit due to the wonders of [unobtrusive Javascript](http://en.wikipedia.org/wiki/Unobtrusive_JavaScript) (I got to throw out alot of "remember to call this function whenever you send a header" cruft in the code).

PS: Other things I like about jQuery (other than the 20KB filesize, have I mentioned that yet?) include a rather sane API (I particularly like the whole $('#foo').val() as a getter, $('#foo').val('bar') as a setter business), in depth documentation with examples (Scriptaculous is somewhat notorious for a "[whoo I make things ANIMATE](http://books.slashdot.org/comments.pl?sid=338261&cid=21104693)" approach to documentation)

PPS: We here at Wejoinin are environmentally conscious, we conserve those bytes because one day they'll all go extinct, and we'll be forced to shout packets at each from hilltop to hilltop instead of sending email. (And reordering packets in your head? Ouch.)
