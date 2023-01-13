---
title: Greater styling control over type with `initial-letter`
description: An overview of the new CSS property `initial-letter` for more styling control over the first letter. 
date: 2023-01-12
tags:
  - web platform
  - css
layout: layouts/post.njk
permalink: posts/2023/1/css-initial-letter/index.html
---

Today we're taking a look at another new addition to CSS that's about to land in browsers: `initial-letter`. This property is still experimental with support in Safari but it is supported in Chromium Canary browsers. It is a bit buggy at times and I encountered issues with DevTools crashing on me so it's still obviously experimental.

## What is `initial-letter` and what does it do?

The CSS property `initial-letter` brings more control and styling over the first letter in a block of text...meaning we can get a little bit more fancy with our typography without hacky tricks.  

`Initial-letter` is a property that applies to the pseudo element `::first-letter`. It lets you control the size of the first letter with a number that indicates how many lines tall the letter should be, and another value, an integer that can be added to indicate how many lines down the letter should sink. 

For example, let's say we want our letter to be 3 line lengths tall. We would write the following:

```
p::first-letter {
  initial-letter: 3;
}
```

And in turn this would render the letter 3 lines tall: 

![alt: Our first letter of each paragraph is 3 lines tall](/img/2023/initial-letter/il-3.png)

Let's bring in the second value to change where the letter is. The letter will still be 3 lines tall but we want it to sink to the fourth line.

```
p::first-letter {
  initial-letter: 3 4;
}
```

![alt: Our first letter of each paragraph is 3 lines tall and sinks to the fourth line](/img/2023/initial-letter/il-3-4.png)

Pretty neat and it only takes a line of code!

## What does this solve for developers?

The power of this property lies in the ability to remove hacks around styling and positioning the first letter of a block of text. There's no wrapping of your first letter in a `<div>` or anything like that. The ability to size based on line height scales the letter nicely too. 

## More examples

Let's look at a more styled demo. You can find the source code on my demo page: [CSS initial-letter demo](https://stephs-demos.netlify.app/initial-letter/).

Technically we are able to size the first letter based on line height with `font-size: 2lh;` or however many lines you'd like the letter to be tall. But we get the following with that declaration: 

![alt: Our first letter has a font size of 2lh applied](/img/2023/initial-letter/2lh.png)

It doesn't quite look right especially when I want to create a really illustration focused first letter. The same thing happens if I try a value of `4lh`...

![alt: Our first letter has a font size of 4lh applied and there is a massive gap below the first normal sized line of text](/img/2023/initial-letter/4lh.png)

It may be 4 lines high but it continues to create a massive gap below the first line. It doesn't align well with the rest of the type either.

When I use initial letter to handle my sizing though, I get the following design with a letter that aligns nicely to the left of the normal sized text and is actually positioned as 4 lines tall. 

![alt: Using initial letter ](/img/2023/initial-letter/initial-letter.png)

The important bits of CSS for the above display are as follows: 

```
  initial-letter: 4 6;
  padding: 2.2rem 2.6rem;
  font-weight: 900;
  margin-right: .5rem;
```

I've added some padding and font weight to control the styling of the first letter a bit more. 

You can inspect the demo for the full set of styles. I would like to note that outlining your letter doesn't appear to work if you have initial-letter applied, which seems like a miss in functionality. I've achieved the outline effect with a text shadow for this demo.

I added an SVG background for the illuminated text treatment, and there's probably some neat animation effects you could apply. 

## Other notes

This is just the start of `intial-letter`, per the [Chromium issue](https://bugs.chromium.org/p/chromium/issues/detail?id=1276900), there are still items in the works: 

Following CSS properties are not implemented yet:
 * `initial-letter-align`
 * `initial-letter-wrap`

And following features are not implemented yet:
 * multi-character initial letters (such as for first word or first phrase styling)
 *  inside-positioned ::marker pseudo-elements
 *  inline-level boxes that are placed at the start of the first line
 * atomic inline

So stay tuned for more to come. 

### Browser support 

As of right now, `initial-letter` is supported in Safari, though [caniuse](https://caniuse.com/?search=initial-letter) says the implementation is incomplete, and it is coming soon to Chromium. 

I'm working in Edge Canary (Chromium) with the experimental web platform feature flag turned on, and the feature just shipped in the beta version of Chrome 110. 

Firefox doesn't appear to be support at all though there was a little bit of movement on the Gecko issue for it, but anything beyond that doesn't seem to be clear. Hopefully it will be prioritized as this feature brings some easy to implement capabilities for good typography on the web.


## Resources 

Here's my [demo page](https://stephs-demos.netlify.app/initial-letter/) link
[A basic codepen](https://codepen.io/seaotta/pen/OJwmpWj)
[MDN Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/initial-letter)
