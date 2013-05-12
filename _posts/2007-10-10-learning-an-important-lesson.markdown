---
author: andrewhao
comments: true
date: 2007-10-10 01:42:31
layout: post
slug: learning-an-important-lesson
title: RSS feeds gone haywire!
wordpress_id: 13
categories:
- Site News
---

Filed under "Dumb things to do to a production Web site":

We apologize! We broke the site for you IE and Safari users for a couple days this week (you may have noticed that visiting a sheet caused your browser to detect and read a [RSS feed](http://en.wikipedia.org/wiki/RSS_(file_format))). We had rolled out a few new features involving RSS feeds for sheet administrators but because we're a little too Firefox-happy, we neglected to check how it reacted with IE and Safari.

Totally our fault! Let us know if it did anything terrible and we'll do our best to make it up to you.

(PS: If you're an administrator you'll see a little RSS feed icon in your browser upon visiting your own sheet. You'll be able to start subscribing to these to monitor signups as they come in!)

Your friends,
-Andrew and Hsiu-Fan

PPS: read on for the gory details!

<!-- more -->

Basically, IE and Safari aren't so nice. When your browser contacts the server it says "hey, I'd like some HTML please!" (and a number of formats, listed in order of which it'd rather receive). We use Ruby on Rails, and assumed the [respond_to magic](http://weblog.rubyonrails.org/2006/03/28/rails-1-1-rjs-active-record-respond_to-integration-tests-and-500-other-things/) would just do the right thing.

It doesn't, IE just tells the server "whatever you can send, I'll take it"! Rails looks at it and says "alright, I'll just give you the first one". So you are forced to order items in the respond_to block with the topmost one being the one you usually want to send. This is really gross and hack-y and [totally better explained elsewhere](http://rituonrails.wordpress.com/2006/12/10/strane-behaviour-of-respond_to-in-ie/#comment-39).
