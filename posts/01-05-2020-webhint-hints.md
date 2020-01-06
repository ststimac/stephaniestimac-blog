---
title: 5 of my favorite hints in the webhint browser extension
description: 
author: Stephanie Stimac
date: 2020-01-05
tags:
  - webhint
  - devtools
layout: layouts/post.njk
---

Full disclosure, the [webhint](https://webhint.io) project is near and dear to my heart. It's a project I've been the lead designer and front-end dev for since 2017 and [Nellie the Narwhal](https://github.com/webhintio/artwork) is my baby. Though my focus at work has shifted away from designing full-time, I still pop in to fix or oversee design updates to the website. 

But that's not why I'm writing this post, I want to highlight just a few of the things that the webhint browser extension checks for when you scan a website from your DevTools. 

You can download the DevTools Browser Extension for [Chrome](https://chrome.google.com/webstore/detail/webhint/gccemnpihkbgkdmoogenkbkckppadcag), [Edge](https://microsoftedge.microsoft.com/addons/detail/mlgfbihcfnkaenjpdcngdnhcpkdmcdee) and [Firefox](https://addons.mozilla.org/en-US/firefox/addon/webhint/). 

If you install the extension and don't immediately see the 'Hints' panel, check your overflow menu, circled here:


![alt: Hints panel in DevTools](../../img/post-8/webhint-devtools.jpg)

Now, onto some of my favorite things that webhint checks for with the browser DevTools extensions.


## 1. Scoped SVG Styles

webhint will check to see if any SVG styles are affecting elements in the DOM outside of the SVG. The webhint browser extension will tell you what CSS rule is causing an issue and the HTML elements being affected. 

Here's an example from webhint that would trigger the hint. 

```
<html>
    <body>
        <h1 class="my-style">Heading</h1>

        <svg>
            <style>
                .my-style {
                    opacity: 0.5;
                }
            </style>
            <text class="my-style">SVG text</text>
        </svg>
    </body>
</html>
```
Here's the detailed webhint documentation on [scoped-svg-styles](https://webhint.io/docs/user-guide/hints/hint-scoped-svg-styles/).



## 2. Supported CSS Features

A lot of web developers have to support Internet Explorer still or just older browser versions in general. This happens in the enterprise space frequently because the cost of upgrading can be substantial therefore limiting how quickly enterprises upgrade. 

So if you're building something that needs to be supported on IE but still want to use newer web technology, webhint can help you out here. 

On my website for example, the hint gets triggered by `display: grid;` and throws the following: 

> 'display: grid' is not supported by Internet Explorer. Add 'display: -ms-grid' to support Internet Explorer 10+.

It will also show me which file, the line location and code. 

![!alt: webhint browser extension screenshot](../../img/post-8/webhint.jpg)

You can actually click on the file in webhint and it will pop you over to the DevTools Sources panel to the problematic spot in your code.

![alt: sources panel in DevTools](../../img/post-8/sources.jpg)

Here's the detailed webhint documentation on [supported CSS features](https://webhint.io/docs/user-guide/hints/hint-compat-api/css/).

## 3. All of the Accessibility Hints

Ok this is technically 14 hints grouped under one main category. Webhint uses axe for its accessibility check and covers all of the following areas: 

* ARIA
* Color
* Forms
* Keyboard
* Language
* Name role value
* Other
* Parsing
* Semantics
* Sensory and visual cues
* Structure
* Tables
* Text alternatives
* Time and media

A few examples of errors I've seen come up outside of color, which is probably one of the most frequent ones I see. 

**Structure** hint that gets triggered:
> `<li>` elements must be contained in a `<ul>` or `<ol> `

**Name role value**:
> Links must have discernible text 
> `<a href="#" class="search"><i class="fa fa-search"></i></a>`

Webhint will also link you over to the Elements panel to show you where in your HTML the offending element is. You can toggle back and forth between the two panels. 

Here's the webhint documentation on the [axe accessibility check](https://webhint.io/docs/user-guide/hints/hint-axe/).

## 4. No vulnerable libraries 

This hint will check for known vulnerabilities within client-side JavaScript libraries and frameworks detected on the website you're testing against. Webhint uses Snyk's vulnerabilities DB to look these up.

An example that gets thrown on an old WordPress site of mine: 

> 'jQuery@1.12.4' has 2 known vulnerabilities (2 medium). See `https://snyk.io/vuln/npm:jquery` for more information.

Here's the webhint documentation on the [vulnerable libraries](https://webhint.io/docs/user-guide/hints/hint-no-vulnerable-javascript-libraries/).

## 5. External links disown opener

Webhint will check your links that have `target="_blank"` applied to them to make sure `rel="noopener"` (and `noreferrer` for older browsers) are also applied due to a security issue if they're not.

If you're like me, you occasionally forget this or miss it here and there while other links in your site are fine. This is a good but simple backup check. Ultimately web devs are human and might miss something!

Here's the webhint documentation on [external links disown opener](https://webhint.io/docs/user-guide/hints/hint-disown-opener/).

## webhint in your dev cycle

The great thing about webhint is you can use it in many different forms across your development cycle. 

* [Online scanner](https://webhint.io)
* [Webhint CLI](https://webhint.io/docs/user-guide/)
* [VS Code Extension](https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint)
* DevTools Browser Extension for [Chrome](https://chrome.google.com/webstore/detail/webhint/gccemnpihkbgkdmoogenkbkckppadcag), [Edge](https://microsoftedge.microsoft.com/addons/detail/mlgfbihcfnkaenjpdcngdnhcpkdmcdee) and [Firefox](https://addons.mozilla.org/en-US/firefox/addon/webhint/)

And the CLI is extremely configurable: you can write your own hints if webhint is missing something you care about or you can remove something webhint checks for that you *don't* care about.

Webhint is an open source project so check out the different [GitHub repos](https://github.com/webhintio) and start contributing today!