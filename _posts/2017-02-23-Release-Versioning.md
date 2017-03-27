---
layout: post
title:  "Release versioning"
date:   2017-02-26 21:38:27 -0600
categories: versioning semver releases jokes
---

There are several different strategies for versioning releases. I'll cover a few of them quickly.

## Semver

`{major}.{minor}.{patch}`

(or to be a bit more clear)

`{breaking}.{feature}.{fix}`

Add in a new feature? Do a minor bump. Change an API? That's a major. Pretty common, pretty easy, well supported.

## The Git Hash

This is my preferred strategy and one I use for the iris chatbot. Since there are multiple people releasing multiple versions from different branches she doesn't have a "golden release". Instead each release is just the current git hash. This is a bit messier but automatic and avoids versioning confusion.

## The Enterprise

`{major}.{minor}.{patch}{Alpha/Beta/RC}-{optional re-release here}`

For when Semver just isn't enough to capture that you aren't sure what you are releasing.

## The Apple

`Adjective Noun {Meaningless Major}.{Minor that only increments by one}`

Ie `Jackass Koala 5.4`

## Marketing

`{Charge More}.{"Free" upgrade}.{Oops, sorry!}{some letters here to convince you it's stable}`

Queue the

"Free upgrades for life! Now on 1.4.7-Gold2! Upgrade to Version 2 'Lemming' for just $19.99!"

## The Incrementer

`{One number that increments}`

WYVIWYG (What You Version Is What You Get?)

---

:heart:,

VH
