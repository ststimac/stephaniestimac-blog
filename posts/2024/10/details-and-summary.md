---
title: The <details> and <summary> elements are getting an upgrade
description: It's going to be easier to style the '<details>' and '<summary>' elements 
date: 2024-10-31
tags:
  - web platform
  - user interface
layout: layouts/post.njk
images:
    thumb: /img/2024/details-summary.webp
permalink: posts/2024/10/html-details-and-summary-update/index.html
---

Form controls are notoriously difficult to style, something the web community has been talking about for years. In 2019, when I was still at Microsoft, I had been working with [Greg Whitworth](https://gregwhitworth.com/) to start evangelizing the work that was being planned for `<select>`, as well as the [Open UI](https://open-ui.org/) community group that would help bring this plan to life. 

There's a lot that has happened in that five years, and more still to come. Most recently I've seen work being done to improve the customizability of the `<details>` and `<summary>` elements. More stylable accordions. Exciting! 

## Why `<details>` is hard to work with
The `<details>` element is a disclosure widget, which is a piece of UI that has a brief summary or heading and a control to expand the UI to show more details. 

When you use `<details>` however, you don't have a lot of control over customizing it (like a lot of HTML Controls). The little triangle to indicate whether it's open or closed is not easily replaced. Styling or customizing `<details>` just isn't easy, which in turn means developers end up building a custom component for their accordions. 

This ends up creating a lot of unnecessary work. Using existing HTML elements means you get all the security, accessibility and performance benefits that have already been baked in. The browser takes care of all that for you. Rebuilding from scratch means you've got to worry about adding all that back in, especially the accessibility bits. 

But you can't style it how you want to, so you end up building it from scratch anyway. Rinse. Repeat. A tale as old as time. 

## Proposed updates

There's quite a bit being proposed to help make `<details>` more customizable and interoperable between browsers (because no one likes it when browsers make things behave/display differently!)

A few highlights: 

1. Remove CSS `display` property restrictions so you can use other `display` types like flex & grid.
2. Specify the structure of the shadow tree more clearly (this helps with flex/grid).
3. Add pseudo-elements to give access to more parts leading to more stylability
4. Better ability to animate these elements through additional changes (these are a part of a separate work stream but will benefit these elements).
5. Improve `::marker` styling 

The exciting news is items 1 & 3 in the list above should be shipping in Chrome 131 Stable next week (first week of November 2024). This will bring a new `::details-content` pseudo-element to the web, allowing more access to parts of `<details>`.

## Further reading
- [_Improvements to `<details>` styling_](https://github.com/dbaron/details-styling) explainer_ by David Baron
- [Phase 1 proposal](https://github.com/dbaron/details-styling/blob/main/phase-1.md)
- [Chromium Bug](https://bugs.chromium.org/p/chromium/issues/detail?id=1469418)
- [Mozilla Bug](https://bugzilla.mozilla.org/show_bug.cgi?id=1856374)

## A Nod to Open UI
Much of this work to improve form controls is started within the [Open UI](https://open-ui.org/) community group. The community there has been working for years to make progress in this space and getting all the browser vendors to agree and work together is often a difficult and time-consuming task. Cheers to all you do. 