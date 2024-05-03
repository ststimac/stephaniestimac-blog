---
title: Microsoft Edge is deprecating support for -ms-high-contrast and -ms-high-contrast-adjust
description: A PSA about Edge deprecating some legacy CSS properties 
date: 2024-05-02
tags:
  - css 
  - notes
layout: layouts/post.njk
images:
    thumb: /img/2024/high-contrast-01.webp
permalink: posts/2024/05/microsoft-deprecating-high-contrast/index.html
---

Microsoft announced it is deprecating support for the CSS properties `-ms-high-contrast` and `-ms-high-contrast-adjust` in favor of the [forced colors](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/forced-colors) standard.

There will be a deprecation period and there's an origin trial and a feature flag so you can ensure your updated CSS is working correctly. 

All the details are over on the Microsoft Developer Blog:
* [Deprecating support for -ms-high-contrast and -ms-high-contrast-adjust](https://blogs.windows.com/msedgedev/2024/04/29/deprecating-ms-high-contrast/)

Woohoo for less browser-specific CSS! 
