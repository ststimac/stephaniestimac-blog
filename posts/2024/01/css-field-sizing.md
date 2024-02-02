---
title: Better form UX with the CSS property `field-sizing` 
description: A look at the `field-sizing` CSS property and how it could improve web form user experience.
date: 2024-01-23
tags:
  - css
  - user experience
layout: layouts/post.njk
images:
    thumb: /img/2024/field-sizing.jpg
permalink: posts/2024/01/css-field-sizing/index.html
---

One of the more painful experiences I've encountered on the web is filling out a form input that is fixed width. Whatever I've typed becomes cutoff and I can't actually see what I've typed or am typing. 

On desktop, I usually click and drag to highlight the text to see the cutoff text. Mobile can be even more annoying, resulting in trying to copy and paste my text somewhere to ensure I've not misspelled anything or added an extra space. 

You can write some JavaScript to auto-size the input to accommodate the content entered into the input but I'm going to guess it doesn't get used that much. That, or painful interactions just stick out more in my mind than ones that are easy. 

## The `field-sizing` CSS property

Some engineers on the Chrome team have proposed and are working on a CSS solution to this problem with the `field-sizing` property. 

The new property could be applied to the following elements:

- `<textarea>`
- `<input type="text">`
- `<input type="number">`
- `<input type="file">`
- `<select> listbox`
- `<select> dropdown`

## `field-sizing` property values 

There are two values proposed for implementation. 

`field-sizing: fixed;` will keep the current behavior and the form control box won't change in size. It would probably be suitable to retain the current behavior if you know that the text length of whatever is being input will be between certain character lengths that don't get cut off. 

`field-sizing: content;` will disable the current behavior and allow the form size to adjust depending on the content. 

One pain point to note with this is, if you're using `<input type="text">`, you will want to put a min and max-width on the element...otherwise it looks like you could just expand forever horizontally, which in itself wouldn't be a great user experience. 

Expanding vertically with `<textarea>` though, does create a much better experience especially on smaller screens. 

### Code example 

This feature is in Developer Trial behind a flag (Experimental Web Platform features) - in Chrome & Microsoft Edge and is expected to be shipping in Chrome 123 (but Chrome Status hasn't been updated to reflect whether this is actually true or not.)

Open up Canary or Dev browser channels (I'm using Edge Canary), ensure your experimental flag is turned on, and check out the codepen below by adding content to the inputs. The first input won't expand, the second one will.

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="qBvXJXj" data-user="seaotta" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/seaotta/pen/qBvXJXj">
  CSS field-sizing property</a> by Stephanie Stimac 🔮 (<a href="https://codepen.io/seaotta">@seaotta</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

## Resources & Availability 

- [CSSWG GitHub Issue](https://github.com/w3c/csswg-drafts/issues/7542)
- [Chrome Status](https://chromestatus.com/feature/5176596826161152)

I can't find signal from Safari or Firefox on this feature but it is available in Dev Trial in Chrome & Edge. No MDN docs page has been published yet but when it lands, I'll update here. 

I think this will make form UX better but depending on the form you'll have to pay attention to widths. And I'm always in favor of replacing JavaScript with CSS functionality if it makes sense and in this case it does. Less JavaScript bloat is always good.

---

Find me on [Mastodon](https://toot.cafe/@seaotta), [Twitter](https://twitter.com/seaotta), [Instagram (personal)](https://instagram.com/seaotta), [Instagram (tech)](https://instagram.com/web_witch) [YouTube](https://www.youtube.com/channel/UCO6Clt5KKCZmvgJKSbm4iBA) or [Subscribe to my newsletter](https://webwitchweekly.beehiiv.com/).
