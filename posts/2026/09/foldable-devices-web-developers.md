---
title: "A Short Update on Designing for Foldable Devices"
description: Foldable devices don't seem to be disappearing from the market. An update on web platform primitives. 
date: 2026-09-24
tags:
  - web platform
  - notes
layout: layouts/post.njk
images:
    thumb: /img/2026/09/dual-screen-update.webp
permalink: posts/2026/09/an-update-on-designing-for-foldable-devices/index.html
---

And here we are three years after I wrote about the [Google Pixel Fold being announced](https://blog.stephaniestimac.com/posts/2023/05/design-foldable-devices/), followed now with the announcement of the iPhone Duo...(I have questions about the naming by the way).  

Four years ago I was talking about web primitives in the platform for the Surface Duo. My how time flies. 

There are [CSS media features](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/At-rules/@media/vertical-viewport-segments), a [Viewport Segments API](https://developer.mozilla.org/en-US/docs/Web/API/Viewport_segments_API), a [Device Posture API](https://developer.mozilla.org/en-US/docs/Web/API/Device_Posture_API) but Chromium based browsers are the only ones currently supporting these things. 

I haven't been able to find any signal yet on whether Safari will support these things in the web platform as the developer docs focus on application development. 

If you're interested in trying out the platform features, you can emulate the Surface Duo and Galaxy Z Fold in the developer tools. 

And if you're thinking, do I really have to have my website adapt to two screens? The answer is no. Adding a design to an application or dual screen makes sense if you have an experience that has two simulataneous contexts that are useful e.g. a list of email messages/inbox on one screen, an open message, email thread or email composer on the other. 

Here's [one of my talks from 2022](https://www.youtube.com/watch?v=DJZI-C_nrqQ&t) if you're interested in learning more about what's available in the browser for dual screen/foldable devices. 

Happy building :) 

