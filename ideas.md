---
layout: page
title:  "Ideas"
date:   2017-04-03 21:38:27 -0600
categories: ideas projects
---

This is a non-exhaustive list of ideas of projects to make. Of course, the value in such a thing is it's execution, not the raw idea, so this is public. If you happen to hijack one of these, drop me a line and I'll link to your repo. Of course, just because something has been done doesn't mean it can't be done better.

## HTML5 Text Adventures

Porting something along the lines of a [MOO engine](https://www.wikipedia.org/en/LambdaMOO) to HTML5/JS would be awfully handy. Being able to play with others, build little widgets in real time using just descriptive text, etc. Websockets and Console.js make this a pretty straight forward project.

## Reasonably Encrypted Markdown Journal

A few exist but all the ones I've explored have basic security flaws like plaintext passwords or storing the journal entries in plaintext. No need to keep the KGB out, but a basic 256 bit AES cipher wouldn't do no harm. It should be clever roommate safe at least. Electron and your view framework of choice. Please make sure it supports GFM and Yaml frontmatter.

## Plex, but for Comics

Sure, [Ubooquity](https://vaemendis.net/ubooquity/) is a thing, but it lost any claim to being lightweight when it was built in Java. Maybe a good choice for Go since the effort here is quite simple? Most of the work is really frontend.

## Ultra lightweight stats

[Piwik](https://piwik.org/) exists but requires PHP and MySQL so that's pretty much right out. Perfect for Go, or maybe even a Rust/C approach? Tiny, embed a little WebGUI in it using something stupidly simple like Mithril. The whole thing should be <20Mb and use almost no memory.

## Port the HomeBrewery PHB theme to Jekyll

Seriously, this is a thing that needs to happen and is totally [allowed by license](https://github.com/stolksdorf/homebrewery/blob/master/license) (plus stolksdorf is pretty nice).
