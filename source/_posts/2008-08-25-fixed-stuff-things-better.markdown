---
author: DarkWulf
comments: true
date: 2008-08-25 01:11:49
layout: post
slug: fixed-stuff-things-better
title: Fixed Stuff. Things Better.
wordpress_id: 37
categories:
- Development
---

Andrew always promises cool new things (sometimes soon), but today I want to tell you about cool things that are no longer broken.

For awhile now, editing sheets has been finicky to downright broken in IE. I updated the site a few days ago, after fixing it a week ago and waiting awhile to make sure it really didn't break anything else that was important. There were two things that were broken: deleting headers (that is, rows and columns), and changing the number of signups allowed on a slot.Warning: tech nerdery ahead. Read on for the gritty details.

<!-- more -->First off, deleting headers. We have a cool Javascript thing that I threw together to deal with the AJAX interactions inside of tooltips and lightboxes, and for the longest time I thought there was an IE bug in there, but it turns out the problem was more mundane. The submit button was a simple <button>Delete</button>, which for most browsers has an implicit type of "submit", while IE understands the type to be "button", AKA do nothing. We actually have lots of helpers to generate buttons, but in this case, this button was encoded as raw HTML. Easy fix, hard problem to finally track down. (I swear I spent months on this on and off.)

Next up, editing signup sheet cells. I'm going to give you a brief sketch the offending code, and what I changed, because I feel like an idiot for this bug being there. I'm not sure why it worked at all in the first place, but whatever. There is a div that is cleared, and then an AJAX request is fired off with the form (that was contained inside the div) fields' data. Now we save the serialized form fields, clear the form, and submit the data. Somehow every other browser managed to serialize the non-existant form just fine. Crazy.

PS: I'm sharing all this because I feel bad about how broken things are, and kind of want to give you, dear reader, a feel for what kind of stuff is going on here at the red-house-that-is-Wejoinin.
