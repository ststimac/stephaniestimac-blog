---
title: 'When to use CSS text-wrap: balance; vs text-wrap: pretty;'
description: A ruthless look at when to use these two CSS text-wrap values.
date: 2023-10-20
tags:
  - css
  - web platform
layout: layouts/post.njk
permalink: posts/2023/10/css-text-wrap/index.html
---

At the start of the year I had written about how I wanted to spend this year writing about new CSS features landing in browsers. Life happened and it was in my best interest to do things off the web and away from my computer. But I'm picking this back up again because I'm genuinely back in a space to be exploring and creating things again. I wanted to start this little post off like this for anyone else who is struggling with burnout. It's okay to take a break. It's beneficial for your brain and the rest of you. Side projects will always be there to work on.

Now onto good ol' text-wrap. 

I was looking into `text-wrap` and doing some research on the difference between when to use `balance` and when to use `pretty` (both are still experimental, but available in Chrome, Edge and Opera.)

## text-wrap: balance; 

There is a limit on the number of lines that `text-wrap: balance;` will apply to *but* it is dependent on how many lines there are based on the width of your text. `Balance` will only apply to less than six lines. 

In the demo below, if you open the code on Codepen in a supported browser, remove `text-wrap` while the width is 300px, you'll see `text-wrap` has no effect. If you change the width to 600px, add `text-wrap: balance;` back to the CSS - you'll see it does have an effect. 

<div class="codepen-container">
<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="GRPzVLN" data-user="seaotta" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/seaotta/pen/GRPzVLN">
  CSS Text Wrap: Balance Limit</a> by Stephanie Stimac 🔮 (<a href="https://codepen.io/seaotta">@seaotta</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
</div>

With `text-wrap: balance;`, because there's a limit to how many lines the browser will wrap, this should only be used on headlines, headings, and subheadings. Applying it to large paragraphs will have no effect and comes at a performance cost because the browser is trying to calculate optimal balance even though it won't apply anything. 

![alt: A comparison of a heading with text-wrap balance applied vs not applied. One heading is optically balanced. The other is not with two short words that wrap to the second line of the heading. ](/img/2023/text-wrap/balance.png)

The example above shows a comparison of a headline without balance applied and a headline with it applied. The first example doesn't look balanced, whereas the second one does. 


## text-wrap: pretty; 

Text wrap `pretty` is the opposite of `balance` and can be used on entire blocks of text but you're only really going to see a difference on the last four lines of text. It's primary use is to prevent orphans - or one word - on their own line. 

The browser makes calculations to make adjustments for you. "To balance between the typographic benefits and the performance impacts, it adjusts the last 4 lines of paragraphs that meet certain conditions." [Chrome Platform Status](https://chromestatus.com/feature/5145771917180928).

The differences are subtle when `text-wrap: pretty;` is applied.

![alt: A comparison of paragraphs of text. One has text-wrap pretty applied to it and one does not. The one with text-wrap pretty has two words on the last line and the one without only has one word on the last line, an orphan.](/img/2023/text-wrap/pretty.png).

In the image above, the paragraph on the left does not have `pretty` applied and there is one word on the last line. In the paragraph on the right, with `text-wrap: pretty;` applied, there are two words on the last line and you can see the slight adjustments to the last three lines to make that second word wrap. 

Very subtle, but it provides a solution to avoid any hacks around trying to get rid of those orphan words that visually look out of place on their own line. 

Support for `pretty` is again quite sparse, with only Chromium browser support. Hopefully Firefox and Safari will ship these to help improve typography on the web. 

## Balance and Pretty

Use `text-wrap: balance;` on headings and subheadings. And use `text-wrap: pretty;` on paragraphs of text to get rid of orphans on the last line. Despite the Chromium-only support, these would be a good candidate for progressive enhancement. It won't negatively affect the experience if someone is not in a supported browser, but it will some visual balance to the page for those in a browser where supported.

Here's the [link out to MDN for text-wrap](https://developer.mozilla.org/en-US/docs/Web/CSS/text-wrap).



-----

Follow me on [Mastodon](https://toot.cafe/@seaotta), on [Twitter](https://twitter.com/seaotta) or [Instagram](https://instagram.com) and yes I'm on Threads too. I run [The Web We Want](https://webwewant.fyi), a place for web developers and designers to submit the things they need from browsers and the web platform to make their jobs easier. 

Author of [Design for Developers](https://www.manning.com/books/design-for-developers?utm_source=stimac&utm_medium=affiliate&utm_campaign=book_stimac_design_4_19_22&a_aid=stimac&a_bid=5f6ba095). 

[Subscribe to my newsletter](https://webwitchweekly.beehiiv.com/) to stay up to date with me, get interesting web platform and design related links.