---
title: A love note to CSS
description: CSS is so incredibly powerful
date: 2023-01-11
tags:
  - web platform
  - css
layout: layouts/post.njk
permalink: posts/2023/1/css-love-note/index.html
---

I was designing a little basic [one page checklist](https://pwa-checklist.netlify.app/) for PWA design best practices based off a talk I gave last year (and will give again this year). I may have overdesigned it a bit but I wanted the headings to sit on top of the containing box's top border.  

I positioned those headings with `position: absolute;` so they were removed from the layout of the rest of the content and therefore couldn't affect anything below them. Two of my headings span two lines on small devices and this was making the content too tight together. Adding a different CSS variable for spacing was changing all of the margins on the `<article>` elements which I didn't want for the top one. Hmph. 

But wait. 

`h2.section-header.long + article` will target the `<article>` elements after any `<h2>` elements with the `.section-header` and `.long` classes. 

And there we go. More space on small screens just where I need it.

## Update

Jhey just showed me the `<legend>` element, which didn't come to mind when building this but would work because I have a set of sectioned checkboxes. I haven't checked to see how easy it is to style but my point still stands that CSS is powerful. 
