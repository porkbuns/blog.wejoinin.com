---
author: andrewhao
comments: true
date: 2007-08-17 00:23:30
layout: post
slug: why-go-fluid
title: Why go fluid?
wordpress_id: 7
categories:
- Design
- Development
---

One of our design decisions was to go with a fluid layout. This meant that the main content was going to expand horizontally with the browser

We noticed quite a few folks using layouts with multiple columns. And as we know, those columns get darn unwieldy when you try to stuff more than three. With a fixed layout, the columns were suffocating the cell content

So we decided to design for those of you with high resolutions (greater than 1024x768) and let you guys put that extra screen width to use.

A very interesting point: the fluid layout, when it becomes too wide, makes text nearly unreadable (longer lines of text increase visual complexity) and single-column tables, well, awkward. We had tossed around ideas of single-column signup sheets staying in a fixed-width layout, then going into an elastic layout once the layout exceeded _x_ number of columns

With design, there's always a tradeoff. Man.
