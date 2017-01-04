---
layout: post
title:  "How to talk about tech: a primer"
date:   2017-01-03 12:00:00 -0600
categories: tech blogging
---

Everyone has read a blog post that starts with a grand claim such as "MyLatestDB is the fastest database ever!", or more than likely, "LatestHatedTech is the worst thing ever made ever." It's probably pretty obvious the issue with this and instead of ripping apart this approach I'm going to recommend a better one. My goal here isn't to be exhaustive, but provide a general guide of how to write blog posts about tech appropriately.

## Define a narrow scope

A really bad claim is as follows:

> jQuery sucks.

Here's a slightly better claim:

> jQuery sucks because it's not a coherent framework.

But the best sort of claim is something like this:

> jQuery is a poor choice for a coherent framework because it's intended to be a toolbelt, and falls short of many alternatives such as backbone or marionette.

It would be difficult to select any technology that is a wholesale failure. Often times technology is abused in ways it wasn't intended to be used and is therefore not exactly ideal. When we claim a technology is bad, we need to be specific about in what aspect. Do we dislike it for its performance? Its lack of features? How does this compare to its intent and its common usage?

## Pros and Cons

An overall better way to discuss technology is to compare and contrast, to discuss pros and cons especially compared to a similar technology. Consider the following:

> Express
> --
> Fast, Connect based
> Lean, minimalistic
> Extremely flexible

> Hapi
> --
> Opinionated
> Batteries Included
> Consistent Performance

All of a sudden instead of making a broad and difficult to support statement ("Express is better than Hapi" or vice-versa), I've delineated their differences because frankly they have very different goals. Express is for those who want a minimalistic starting point that is highly configurable. Hapi is batteries included for those that want traditional, consistent applications. Neither is inherently better or worse, but each one is better for a given goal.

## Weigh and discuss alternatives

Even if my goal is to be critical of a technology, I need to be able to point to alternatives that meet the burden I'm attempting to place. Not all of these alternatives are likely to be equally good, but we can insert a discussion about them.

> MySQL is a poor choice for time series data. Instead we can look to purpose built products such as InFluxDB or Riak. InfluxDB supports user permissions and several other basic features but lacks the powerful distributed capabilities of Riak.

## In Short

Use your words and form coherent arguments. Don't just trash tech (though I realize it's edgy and probably helps your impressions) but instead keep in mind the actual goal of that tech, and that it was in fact made by other humans.
