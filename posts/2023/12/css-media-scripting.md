---
title: CSS Media Query for Scripting Support
description:
date: 2023-12-01
tags:
  - css
  - web platform 
layout: layouts/post.njk
permalink: posts/2023/12/css-media-query-scripting/index.html
---

Chrome 120 was released last week and in this version, we got the CSS Media Query for scripting support. Simply, this media query allows you to test whether scripting language are available and tailor page content and styles depending on support. 

## Media query syntax 

There are three values to choose from for the media query: `none`, `initial-only`, and `enabled`.

The value `none` means that the user agent won't run scripts for the current document, either because it doesn't support it or support isn't active for scripting. 

The value `initial-only` means that scripting is available during the initial page load, but not after. 

The value `enabled` means scripting is supported and active for the current document and the "lifetime" of the document. 

### Code Example

The CSS media query means you can change the styling and content of the page based on a class name. You could have three different sets of content built out in your HTML, and depending on the status of scripting you can show one of those content sets while hiding the other two. 

``` 
<div class="no-scripting">
No scripting so here's a specific set of content and styles 
</div>

@media (scripting: none) {
    .no-scripting {
        display: flex;
        color: green;
    }

    .initial-scripting {
        display: none;
    }

    .full-scripting {
        display: none:
    }
}
```

## Support

The CSS media query for scripting support is available in Chrome as of November 29, 2023, and was already available in Firefox and Safari (both released earlier this year in May and September, respectively). Support is coming in Microsoft Edge and Opera, where the feature is currently in preview. There is no apparent signal from Samsung Internet, with no support at all for the feature.  

## Closing 

This seems like a pretty great feature for progressive enhancement even at the most basic level. You can ensure your users who have JavaScript support disabled get a good experience fairly easily.  With nearly full major browser support, this is a great addition to the web platform. 

Happy coding!

Edit after publishing: There is indeed a `<noscript>` tag, but the intention with this media query "isn't to replace noscript. Its just to allow you to style elements based on the script state." - [Source Link](https://bugs.chromium.org/p/chromium/issues/detail?id=1467097)