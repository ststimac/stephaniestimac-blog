---
title: CSS Media Query Support for Video <source> Elements
description: A brief note on HTML video and media query support
date: 2023-12-06
tags:
  - css
  - web platform
  - notes
layout: layouts/post.njk
images:
    thumb: /img/2023/video-source-elements.webp
permalink: posts/2023/12/css-media-video-source/index.html
---

I've been digging around on web platform status pages to see what's come out and what's planned for web developers. You can take the girl out of browser work but you can't take browser work out of the girl. Or something like that.

Here's another media query that recently was reintroduced and brings back support for video `<source>` elements. It just shipped in [Chrome 120](https://chromestatus.com/feature/5144127067127808), as well as Firefox 120 which included a patch for it. It's also supported in Safari. Additional Chromium browsers such as Microsoft Edge and Opera should receive the update from Chrome.

This gives us another option for responsive HTML video and has web performance benefits.

## A Brief Code Example

You can offer alternative source files depending on the `media` condition.  

```
<video controls>
  <source src="video-large.webm" media="(min-width: 900px)" />
  <source src="video-medium.webm" media="(min-width: 600px)" />
  <source src="video.webm" />
</video>
```

This is just a brief code example of how it looks. Scott Jehl wrote a great [in depth article](https://scottjehl.com/posts/using-responsive-video/) with all the details. He's also responsible for the Firefox patch. 

Thanks Scott! 