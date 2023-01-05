---
title: An Intro to Trigonometric CSS Functions
description: Taking a look at Trigonometric CSS functions and what problems they solve
date: 2023-01-04
tags:
  - web platform
  - css
layout: layouts/post.njk
permalink: posts/2023/1/css-trigonometric-functions/index.html
---

While perusing the [December 2022 post from web.dev](https://web.dev/web-platform-12-2022/) about what's new in the web platform, the addition of Trigonometric CSS functions in Firefox caught my eye. 

Geometry and trigonometry were my two best math areas in school (I am not an Algebra person and generally did not enjoy math class), so I wanted to a quick look at these functions and what problems they solve for the web platform. When would developers use them?

## Trigonometric CSS Functions Overview 

As of December 2022, Firefox and Safari are the two mainstream browsers that support Trigonometric CSS Functions. These include `cos()`, `sin()`, `tan()`, `asin()`, `acos()`. `atan()`, and `atan2()`. 

Support in Chromium is estimated to ship in version 111. 

### Basic use cases per the MDN documentation

- `cos()`: can be used to keep the size of a [rotated box](https://developer.mozilla.org/en-US/docs/Web/CSS/cos#keep_the_size_of_a_rotated_box)
- `sin()`: can be used to [size boxes](https://developer.mozilla.org/en-US/docs/Web/CSS/sin#boxes_size) and as an [`animation-duration` value](https://developer.mozilla.org/en-US/docs/Web/CSS/sin#controlling_animation_duration)
- `tan()`: can be used to [draw parallelograms](https://developer.mozilla.org/en-US/docs/Web/CSS/tan#draw_parallelograms)
- `asin()`: can be used to [rotate elements](https://developer.mozilla.org/en-US/docs/Web/CSS/asin)
- `acos()`: can be used to [rotate elements](https://developer.mozilla.org/en-US/docs/Web/CSS/acos#rotate_elements)
- `atan()`: can be used to [rotate elements](https://developer.mozilla.org/en-US/docs/Web/CSS/atan#examples)
- `atan2()`: can be used to [rotate elements](https://developer.mozilla.org/en-US/docs/Web/CSS/atan2#rotate_elements) and accepts two values as parameters

The MDN docs highlight the differences between the 4 functions for rotating elements. For example, `atan()` returns the inverse tangent of two values between -infinity and infinity, whereas `sin()` returns the sine of a number that has a value between -1 and 1.  


## What problems do they solve for developers?

At first glance, the use cases for these functions don't seem incredibly compelling to me. The MDN documentation use cases for rotating a shape or defining widths of elements don't seem that useful for a developer. We can already do those things and the examples with these functions seem long winded. 

So I went and found the [CSSWG GitHub discussion](https://github.com/w3c/csswg-drafts/issues/2331) to dig into the "why?"

The main takeaway: these additions to CSS mean more complex animations that can be built with CSS and not JavaScript. This [animation example from Ana Tudor](https://codepen.io/thebabydino/pen/JNZGwE/) is a good example. Trigonometric computations are done in JavaScript to achieve a seamless animation effect where the points line up exactly as they rotate and when the orange shapes skew on each rotation.

Another possible use case that came up elsewhere was using these to create charts and graphs in CSS, but this raises a question around responsiveness and scaling those angles and curves, though responsive skewing is mentioned in the GitHub issue.

## Closing thoughts 

The addition of more math functions to CSS reduces some reliance on JavaScript which I view as a win. The primary use case for these seems to be easier shape creation and more options for building complex animations. 

If you're building and maintaining an average website, I don't see these being overly useful, but I'd love to know if you have a use case for these functions. Let me know on [Twitter](https://twitter.com/seaotta) or [Mastodon](https://toot.cafe/@seaotta).


## Resources: 

- [CSS Values and Units Modules Level 4: Trigonometric Functions](https://www.w3.org/TR/css-values-4/#trig-funcs)

- [Part 1: in CSS and JavaScript: Introduction to Trigonometry](https://tympanus.net/codrops/2021/06/01/trigonometry-in-css-and-javascript-introduction-to-trigonometry/) by Michelle Barker
- [Part 2: Trigonometry in CSS and JavaScript: Getting Creative with Trigonometric Functions](https://tympanus.net/codrops/2021/06/02/trigonometry-in-css-and-javascript-getting-creative-with-trigonometric-functions/) by Michelle Barker
- [Part 3: Trigonometry in CSS and JavaScript: Beyond Triangles](https://tympanus.net/codrops/2021/06/04/trigonometry-in-css-and-javascript-beyond-triangles/) by Michelle Barker

---

Want to keep in touch? Sign up for my [newsletter](https://webwitchweekly.beehiiv.com/) to stay up to date with [my book](https://www.manning.com/books/design-for-developers?utm_source=stimac&utm_medium=affiliate&utm_campaign=book_stimac_design_4_19_22&a_aid=stimac&a_bid=5f6ba095) (including sales), upcoming projects and events, and other bits about cool things on the web.