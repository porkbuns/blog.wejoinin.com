---
author: andrewhao
comments: true
date: 2007-10-11 17:58:22
layout: post
slug: lessons-learned
title: Lessons learned
wordpress_id: 14
categories:
- Development
- Site News
---

Man, we totally screwed this one up.  This week's RSS mishap led some users' sheets to lose several signups.

One of the dumb things that we forgot to do was ensure a backup system was in place. Since we hang out at [Dreamhost](http://www.dreamhost.com), periodical MySQL backups aren't provided. And since we're a small two-dude operation (and we only have time to work on this on the weekends), we tend to focus on development and completely overlook small, important things. Like periodically backing up our databases.

So when my friend Joe asked me to back up his sheet (they're using it over at [UCSD Intervarsity](http://www.ucsdiv.org)), I momentarily panicked. Where's our database backups? Oh wait, _we don't do that._ Doh! Why didn't we write the simple shell script earlier?

Thankfully, we inspected our Rails production log and manually extracted the pertinent signups and re-inserted them back into the application. Man, it was no small feat. Then I spent five minutes writing the shell script and cronjob I should have done months ago.

I learned my lesson. Prepare for the worst, because Murphy's Law is alive and well on the 'Net. Have contingency plans in place. Don't. be. stupid (argh!).

Did your sheet lose a signup? Now would be a great time to check and [let me know](mailto:andrew@wejoinin.com). I'd be more than happy to restore them for you.

A little wiser,

-Andrew
