---
title: The Curious Case of the CSS Monochrome Media Query
description: 'Attempting to solve the puzzle of the existence of @media: monochrome'
date: 2024-03-29
tags:
  - web platform
  - css
layout: layouts/post.njk
images:
    thumb: /img/2024/monochrome.webp
permalink: posts/2024/03/css-monochrome-media-query/index.html
---

I make a habit of browsing web platform features to see what's new and interesting and moving along in the browser space. It also leads to discovering things that have been around a while that I haven't heard of before. 

In one such instance, this is how I discovered `@media(monochrome)`. I found this media query particularly relevant with what seems to be an onslaught of e-ink devices making their way into the market. Someone tweeted about their [Boox Palma](https://shop.boox.com/products/palma), and it seems in this instance, a media query to target monochrome UI just makes sense. 

I tried testing the monochrome media query on my Kindle browser with this [quick demo*](https://stephaniestimac.com/demos/monochrome/). If the device is monochrome, that message should change to say your device supports monochrome. 

My Kindle didn't though. It said it wasn't a monochrome device which is obviously wrong and boils down to the browser. ([This person also tried the same on their Kindle and got the same result](https://www.quirksmode.org/css/mediaqueries/color.html)).

I don't know what browser my Kindle has, though the device is at least 4 years old and no more than 5. Googling brought up some obscure Stack Overflow threads about the Kindle browser not being modern enough to support media queries. But according to caniuse.com, this feature was supported as far back as Chrome version 4. 

Curious. 

In 2022, a WebKit bug that had been opened [since 2013](https://bugs.webkit.org/show_bug.cgi?id=112549). This must have relevance somewhere in order to make a fix to match the spec.

But there is very little information on it otherwise. A few mentions of using it for print layouts, but there's a media query to target print layouts already. Most sites that have posted about it are just regurgitating the very minimal information the spec provides. 

Does it even actually work as intended? There doesn't seem to be a way to test without a monochrome device. But which types of monochrome devices it supports isn't documented anywhere.

In theory, it seems like it would be the perfect CSS feature to provide designs tailored to a monochrome device and these e-ink phones are slowly starting to appear. If you have an e-ink device with a modern browser and click the demo link I've shared above, I'd be much obliged to know which message you get. 


---


*It was a very quick demo, and therefore it says "dual screen device demo in the meta information so just ignore that please