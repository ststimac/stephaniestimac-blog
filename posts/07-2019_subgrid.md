---
title: First thoughts & musings on playing with CSS Subgrid
description: A post on initial CSS Subgrid experiements
date: 2019-07-09
tags:
  - css
  - subgrid
layout: layouts/post.njk
---

<p class="blog-post__date">9 July 2019</p>

First things first: CSS Subgrid is currently available in Firefox Nightly. In order to view this experiment properly, you've got to install Firefox Nightly. This isn't a particularly in-depth experiment or demo with CSS Subgrid but rather I wanted to get a feel for what it could do and start to brainstorm use cases. 

Here is some initial reading/watching/listening to do on Subgrid:
- Rachel Andrew talked about Subgrid at CSSConfEU: [Hello Subgrid](https://www.youtube.com/watch?v=vxOj7CaWiPU)
- [MDN Docs: CSS Subgrid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Subgrid)

## Subgrid: What is it?

Currently in CSS Grid, when you create a grid container inside another grid container, the nested grid is independent of its parent grid. With Subgrid, in your nested grid container, you can apply 
`grid-template-columns: subgrid;` and/or `grid-template-rows: subgrid;` and your nested grid with inherit the parent's column, row and gap sizing. You can choose to have your nested grid item inherit both columns and rows from its parent or just one of them. 

## Example with `grid-template-columns: subgrid;`

In this example, I've created a grid container and nested div that I've placed along the parent grid. This nested div spans from columns 3 to 11 and rows 3 to 6. 

I then apply `display:grid;` to the nested div and then add `grid-template-columns: subgrid;` which will inherit the parent grid's column tracks. 

![alt: subgrid exmaple](../../img/post-1/grid-1.png)

For this example, I set a different row height, independent of the parent grid, to repeat 4 times at a height of 40px. Here, my subgrid actually extends past the rows I said my nested item would span (rows 3 to 6), and the background color I've applied to my subgrid actually stays confined to those rows of the parent grid, hence the overlap effect with item 10.  

![alt: subgrid exmaple](../../img/post-1/subgrid-2.png)

But the important part here is that the nested grid is inheriting the parent grid's column tracks by simply using `grid-template-columns: subgrid;`. Here's a codepen of the current example:

<div class="codepen">
<p class="codepen" data-height="265" data-theme-id="0" data-default-tab="css" data-user="seaotta" data-slug-hash="pXQeYa" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="Basic Subgrid Example">
  <span>See the Pen <a href="https://codepen.io/seaotta/pen/pXQeYa/">
  Basic Subgrid Example</a> by 🌙 Stephanie (<a href="https://codepen.io/seaotta">@seaotta</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
</div>

## A larger subgrid columns example

Again, this next example focuses mostly on utilizing subgrid to inherit column tracks from the parent grid. I am currently working on another example that uses `grid-template-rows: subgrid;` for another post, but because of the tendency for things to be laid out in a vertical rhythm on the web, most of my ideas for exploring subgrid have been around inheriting the parent grid's columns. 

You can find the full page of this example under my CSS Grid Experiments: [CSS Subgrid & Good Omens](https://stephaniestimac.com/css-grid-experiments/project5/good-omens-subgrid), and yes, I am a huge nerd because the Good Omens adaptation delighted me so much I dropped in quotes from the book and photos from the show because one should love what they create. 

![alt: larger layout example](../../img/post-1/good-omens.png)

I won't go into as much detail with this layout, but explain briefly what I did. 

I setup the parent grid with the intent to have chunks of text that span 4 columns and then have a nested section under those chunks of text with 4 distinct columns and content that inherit the parent grid's columns and gaps. 

Within the first subgrid, I've explicitly defined where each column should be placed and how many rows it should span and we get the illusion of a layout that may be complicated if trying to replicate using something other than grid. 

![alt: subgrid with 4 columns](../../img/post-1/subgrid-go.png)

I then place another block of text below this nested grid container (and placed on the parent grid.) Below this, I created another nested grid container item, inheriting the parent grid column tracks again and perfectly aligning the columns to the parent and the first nested subgrid layout. 

![alt: subgrid with 4 columns](../../img/post-1/bottom-subgrid.png)

And then because I can, I placed another item on the parent grid that is top-aligned with the second subgrid by sharing the same row start. Ta-da!


## Overall thoughts

Subgrid makes alignment within a large layout much easier to manage. This post with the examples was just a way for me to start to dip my toes into what's possible with subgrid & I hope to work on a few more posts with patterns that would benefit and be simplified by the use of subgrid.

As someone who works on the DevTools UX for Edge, I even have a few ideas around how to improve the experience for viewing subgrid in the DevTools but first other browsers need to start implementing the spec for it. 

Stephanie 

