---
title: Serving less data to users with the `prefers-reduced-data` media query
description: An overview of the proposed CSS media query `prefers-reduced-data` 
date: 2023-04-16
tags:
  - css
  - performance
  - web platform
layout: layouts/post.njk
images:
    thumb: img/2023/prefers-reduced-data.png
permalink: posts/2023/4/css-prefers-reduced-data/index.html
---

I want to take a quick look at another experimental CSS feature today that's focused on tailoring what gets served to a user based on their preferences, but this time it's performance based. 

Similar to media queries like `prefers-reduced-motion` and `prefers-color-scheme`, the media query `prefers-reduced-data` would allow developers to serve up a separate set of styles for those who want to limit the amount of data that gets downloaded. There are a multitude of reasons someone may want to reduce the amount of data being downloaded (Read: [Location, Privilege and Performant Websites](https://blog.stephaniestimac.com/posts/10-30-2019-performance/)). 

It's a CSS media query so it gets inserted into a CSS stylesheet and can either be set to to `prefers-reduced-data: no-preference` or `prefers-reduced-data: reduce`. Immediately the two resource consuming items that can be controlled via CSS that come to mind are fonts and images. 

You can serve up smaller or no images, and you can limit the fonts and font styles that are pulled in. At first I thought these would be the main items you'd want to use the media query. But if you're just serving up smaller sized images, this begs the question, shouldn't you be doing that anyway? Everyone would benefit from smaller image sizes. 

The other use case I can imagine is on the extreme end, and is influenced by NPR's [text only website](https://text.npr.org/) they provide for people. You could provide an extremely stripped down version of a website, for the purpose of highlighting the essential content without having to maintain another URL. 

In some ways, this seems like a useful media query, but at the same time I'm prompted to ask: does it fully solve the problem of serving less data consuming experiences to those who want that option? Or are there already other ways to do this effectively outside of a media query?


## Browser support

Whether this really solves the problem of serving less data remains to be seen. The media query is not currently supported in any browser. There had been a little bit of activity on the issue last year but there hasn't been much movement since.

In the Chrome DevTools though, you can [emulate the media query](https://developer.chrome.com/blog/new-in-devtools-86/#emulate-prefers-reduced-data). 


## Information and discussion 

Here's the [Chrome Status](https://chromestatus.com/feature/5922192355229696) link for the feature. If this is something you want to see in browsers and want to help signal that desire and have a discussion around it, I'd suggest submitting the idea to the [Web We Want](https://webwewant.fyi) to track it there (the initiative is starting to kick back up again!). 

