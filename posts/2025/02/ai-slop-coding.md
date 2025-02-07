---
title: The hard truth about using AI in coding
description: Some thoughts on using AI to help you code.
date: 2025-02-07
tags:
  - coding
  - devtools
layout: layouts/post.njk
images:
    thumb: /img/2025/using-ai-coding.webp
permalink: posts/2025/02/thoughts-on-ai-slop-coding/index.html
---

In a recent experience while building a website, I tried to use ChatGPT to help me out with JavaScript. Something I've never needed to fully learn because my work has always been divided by JavaScript devs and HTML/CSS devs. A long time ago I used to be able to write bits in JQuery but that knowledge is long faded. The point is, I've never had to sit down and learn anything beyond the basics of JavaScript because it wasn't required of me. 

While redesigning and building a website for work, I found I needed a bit of JavaScript to get my mobile menu to open and close and thought, why don't I ask ChatGPT what I need. For all my knowledge, I scanned the 10-15 lines of JavaScript that it output, recognized some bits and dropped it into my file. It worked! And then I padded into Jhey's office to tell him of my success. 

"But is the code correct?" He asked. And this, dear reader, is where the hard truth hit me. Jhey looked at the ChatGPT output. It had gifted me 5 lines of completely unnecessary code, and another bit was "fine" but not the most efficient way to write JavaScript. He made a few edits for me and left me to continue on with my CSS overhaul. 

And here's the hard truth: AI is useful *if* you already know what you're doing. I've watched Jhey work through mathematical problems to help him with code and the difference is, he knows when the output that AI is giving him doesn't make sense or is wrong. The same goes for one of my friends back in Washington state, who has been using ChatGPT to help him speed up his work. They have the background and the foundation to prevent them from committing AI slop code. 

I fear for the students who are only relying on AI to teach them code and are blindly trusting that ChatGPT or Copilot knows what they're doing without the foundational knowledge, or even a mentor to tell them, "this isn't correct" and "this doesn't make sense." 

I tried to use AI for some pixel to em calculations and it just couldn't calculate what I needed, I ended up scratchpadding what I needed and adjusting things in the browser DevTools to get what I needed. I have not tried to experiment with AI further as the environmental impact of me just trying to experiment weighs heavy on my mind.

I feel the need to caution, AI is a tool, one of many, but it should not be the only tool in your arsenal as its reliability is fickle. Find books or media from experts to learn from. If you can afford to take a course, do so. If you're a relatively new dev, aim to stand out by understanding what it is AI outputs and be able to say, that can be improved upon and I understand what it means. I have seen many PRs in open source projects be rejected because the code doesn't make sense and the dev who submitted it can't explain what the code means.

I implore you, please don't blindly trust AI to write your code, lest we be overrun by AI slop for the sake of saying, "I used AI" to appease the investors. 