---
title: The Web We Want Survey Results
description: Looking at what the web community prioritizes out of winning Web We Want submissions.  
date: 2020-05-14
tags:
  - web platform
  - web we want
layout: layouts/post.njk
permalink: posts/2020/05/web-we-want-2019-survey-results/index.html
---

<p class="blog-post__date">14 May 2020</p>

At the end of July 2019, we kicked off our first live Web We Want session. At the start, we only had a handful of submissions and one person willing to record their lightning talk for the session we ran at An Event Apart D.C. We've come quite a ways since then with over 250 submissions to the website. 

[Myself](https://twitter.com/seaotta) and [Aaron Gustafson](https://twitter.com/AaronGustafson) have run 5 sessions at conferences and successfully onboarded community members to run an additional 3 sessions at events themselves, resulting in 8 sessions between July 2019 and February 2020. 
 
To start diving into the various Wants that have been submitted, the Web We Want team is initially focusing on the 12 winning Wants from the 6 events that were run last year to start to dig into which of them are the most important problems or areas we should focus on. 
 
Since the Wants fall into different areas and teams, the surveys were divided into three categories: DevTools, HTML/CSS/Layout, and General Browser for more miscellaneous/broader requests. 
 
Each survey asked the following questions for each want: 
 
- On a scale of 1 to 10, 1 being "not useful at all", and 10 be "extremely useful", rate each want on how useful you think it is. 
- Please rank each want from your favorite to least favorite. 
 
A few things to note here: 
 
I started to include a question about the types of roles people consider themselves to be in after the first survey. This can (maybe) help provide more insight into why certain things I was expecting to rank highly, didn't. So that information is missing from the first survey about developer tooling wants. 

For the scale of “not useful at all” to “extremely useful”, this formula uses an NPS or Net Promoter Score, which is usually used to help gauge customer loyalty but in this context is more focused on customer attitudes. 

## DevTools Survey Results

There were 60 respondents to the DevTools survey and these were the 4 Wants: 
 
- [I want to be able to save/load debugger state](https://webwewant.fyi/wants/60/)
- [I want improved behavior of browser emulators to match interaction on mobile devices](https://webwewant.fyi/wants/79/)
- [I want accessibility tools front & center](https://webwewant.fyi/wants/12/)
- [I want a source order viewer for rearranged content](https://webwewant.fyi/wants/64/)

### Scoring how useful each submission would be

It would be useful if Browser DevTools put accessibility tooling in a more prominent and easily findable location.

![alt: NPS Score for prominent accessibility tooling: 12.](/img/survey-results/DevTools/more-prominent-a11y-tooling.png)

It would be useful if Browser DevTools were able to save the current debugger state to a file in order to load and restore the file back into the DevTools to start debugging from the same place.

![alt: NPS Score for saving the current debugger state: -38.](/img/survey-results/DevTools/save-current-debugger-state.png)


It would be useful if the Browser DevTools had a source order viewer built in to identify rearranged content that would cause accessibility problems for screen readers.

![alt: NPS Score: for saving a source order viewer: -18.](/img/survey-results/DevTools/source-order-viewer.png)


It would be useful if Browser emulators did a better job of emulating interaction on mobile devices.

![alt: NPS Score for better browser emulators for mobile devices: 35.](/img/survey-results/DevTools/browser-emulators.png)


### Please rank each of the items from favorite to least favorite. 

These were the results, in order of ranking:

 1.	I want accessibility tools front & center 
  1st choice: 48.3% 
  2nd choice: 21.7% 
  3rd choice: 20% 
  4th choice: 10%
 
 2.	I want improved behavior of browser emulators to match interaction on mobile devices 
  1st choice: 36.7% 
  2nd choice: 35%
  3rd choice: 18.3% 
  4th choice: 10%
 
 3.	I want a source order viewer for rearranged content 
  1st choice: 1.6% 
  2nd choice: 30% 
  3rd choice: 36.7% 
  4th choice: 31.7%
 
 4.	I want to be able to save/load debugger state 
  1st choice: 13.3% 
  2nd choice: 13.3% 
  3rd choice: 25%
  4th choice: 48.4%

![alt: Visual representation of the ranked wants](/img/survey-results/DevTools/rank-devtools.png)

### Notable Verbatims 

A few quotes from survey takers that I thought were worth calling out.

> It would be great if all emulation were in the same place. Device, css prefers color scheme query, high contrast, dual screen, responsive mode, etc.

> I’m all good, just so glad you’re interested in making the tools better

## General Browser Survey Results

There were 67 respondents to the General Browser survey and these were the 3 Wants: 
 
- [I want a standard API for event throttling and debouncing](https://webwewant.fyi/wants/4/)
- [I want browsers to fix automatically fixable accessibility problems automatically ](https://webwewant.fyi/wants/10/)
- [I want browsers to localize data like dates and numbers](https://webwewant.fyi/wants/59/)
 
**49%** said they were full-stack developers
**39%** said they were front-end developers
**7%** said they were in other roles: accessibility consultant, architect, JavaScript developer, Head of Engineering, and "tired old user"
**4%** said they were designers

### Scoring how useful each submission would be

It would be useful is there was a standard API for event throttling and debouncing. 
![alt: NPS Score for a throttling and debouncing API: 3](/img/survey-results/Misc-Browser/throttling-debouncing-api.png)


It would be useful if browsers could localize data like date formatting, currency, time and weight depending on a user's preferences.
![alt: NPS Score for localizing data like date formatting, currency, etc: 18](/img/survey-results/Misc-Browser/localize-data.png)


It would be useful if browsers could automatically fix fixable accessibility issues such as lack of focus indicators, lack of readability because of low contrast text, etc.

![alt: NPS Score for browsers automatically fixing fixable accessibility issues: 15](/img/survey-results/Misc-Browser/localize-data.png)


### Please rank each of the items from favorite to least favorite. 

These were the results, in order of ranking:
 
 1.	I want browsers to localize data like dates and numbers 
  1st choice: 29.8%; 
  2nd choice: 47.8%; 
  3rd choice: 22.4%;
 
 2.	I want browser to fix automatically fixable accessibility problems automatically 
  1st choice: 37.3%; 
  2nd choice: 26.9%; 
  3rd choice: 35.8%;
 
 3.	I want a standard API for event throttling and debouncing 
  1st choice: 32.8%; 
  2nd choice: 25.4%; 
  3rd choice: 41.8%;

![alt: Visual representation of the ranked wants](/img/survey-results/Misc-Browser/ranked-misc.png)

### Notable Verbatims 

Accessibility was the hot topic in the survey comments. 
 
>Accessibility isn't hard - I see no point in automatically fixing it. Please add support for focus-visible, the element() CSS function, subgrid, gap for flexbox, Web Share API level 2, constructable stylesheets, and CSS modules!
 
> The accessibility thing sounds nice in theory but I guess I'd need to see the implementation? I'd like to think my sites are pretty accessible to begin with, and if it ended up being something I had to test against as a developer to make sure it wasn't breaking anything in the design then I'm not sure how it's helping me.

> Please give more focus on accessibility - it would really help all the users while others are like functional/perf related.
 
> If we're going to have good built-in date formatting, we need better date WIDGETS with it. Everyone rolls their own datetime widgets now because of the lackluster browser implementations.
 
## HTML/CSS/Layout Survey Results

There were 104 respondents to the HTML/CSS/Layout and these were the 5 wants: 
 
- [I want better justification (text align)](https://webwewant.fyi/wants/74/)
- [I want better HTML forms ](https://webwewant.fyi/wants/48/)
- [I want semantic HTML sidenotes](https://webwewant.fyi/wants/52/)
- [I want the ability to flow content dynamically from one container to another using CSS](https://webwewant.fyi/wants/80/)
- [I want SVG to be fully styled from CSS](https://webwewant.fyi/wants/25/)

48% said they were front-end developers
40% said they were full-stack developers
5% said they were designers
4% said they were in other roles such as Accessibility consultant, UI Engineer, and a Project Manager
3% said they were back-end developers

### Scoring how useful each submission would be

It would be useful if browsers had better native form control and functionality like a date picker, time picker, dropdowns with values fetched from a server, and better handling of large dropdowns with filters.

![alt: NPS Score for better native form controls: 56](/img/survey-results/HTML-CSS/better-form-controls.png)

It would be useful if I could flow content dynamically from one container to another depending on the available viewport by using CSS.

![alt: NPS Score for better native form controls: -21](/img/survey-results/HTML-CSS/flow-content-dynamically.png)

It would be useful if HTML had a semantic `<sidenote>` element for content such as clarification of words or notes to accompany an article that may keep away from the main story. A footnote tailor for the web and web layouts.

![alt: NPS Score for a semantic HTML sidenote element: -53](/img/survey-results/HTML-CSS/semantic-sidenotes.png)

It would be useful if the web had better text justification (text-align) for layouts, with better hyphenation and advanced line breaking.

![alt: NPS Score for better text justification: 2](/img/survey-results/HTML-CSS/text-justification.png)

It would be useful if I could style SVG completely with CSS and not have to rely on JavaScript for things like repositioning and resizing.

![alt: NPS Score for SVG to be fully styled from CSS: 2](/img/survey-results/HTML-CSS/svg-fully-styled.png)



### Please rank each of the items from favorite to least favorite. 

These were the results, in order of ranking:

 1.	I want better HTML forms 
  1st choice: 67.3%; 
  2nd choice: 11.5%; 
  3rd choice: 5.8%; 
  4th choice: 7.7%; 
  5th choice: 7.7%;

2. I want better justification (text-align) 
  1st choice: 12.5%; 
  2nd choice: 27.9%; 
  3rd choice: 28.9%; 
  4th choice: 16.3%; 
  5th choice: 14.4%;

3. I want SVG to be fully styled from CSS 
  1st choice: 9.6%; 
  2nd choice: 27.9%; 
  3rd choice: 33.7%; 
  4th choice: 11.5%; 
  5th choice: 17.3%

4. I want the ability to flow content dynamically from one container to another using CSS 
  1st choice: 8.6%; 
  2nd choice: 22.1%; 
  3rd choice: 21.2%; 
  4th choice: 33.7%; 
  5th choice: 14.4%;

5. I want semantic HTML sidenotes 
  1st choice: 1.9%; 
  2nd choice: 10.6%; 
  3rd choice: 10.6%; 
  4th choice: 30.7%; 
  5th choice: 46.2%;

![alt: Visual representation of the ranked wants](/img/survey-results/HTML-CSS/ranked-html-css.png)


### Notable verbatims: 

Y'all want container queries. This is a really complex problem and there are a lot of posts out there about it already so I'm not going to dive into this problem here. 

> It would be great if CSS could be applied to the native controls (such as a date picker, time picker, etc), similarly to how we can use appearance: none; on a button to style it in any way we’d like.
 
> Container queries is what we want 😊
 
> Container queries would be a 10.
 
> ELEMENT QUERIES ABOVE EVERYTHING
 
## So what's next?

To be totally honest, this isn’t a straightforward answer as it depends on the Want. Generally DevTools features can be easier to prototype and test and start getting feedback on, but when it comes to web platform features, things are going to take longer especially if standards groups have to be involved. 

Recently, I’ve been involved in conversations with team members working on other browsers, as has my co-worker [Aaron](https://twitter.com/AaronGustafson), about the Web We Want and how we integrate the submissions with other signals from the web community. We're still smoothing out the process, so if you have feedback on how you'd like to see browsers work with the feedback, feel free to engage with us on [GitHub](https://github.com/WebWeWant/webwewant.fyi) or [Twitter](https://twitter.com/webwewantfyi). 

The point I want to highlight here is we are working with other browser vendors to look over everything that has been submitted and are assessing whether it's something already being worked on by browsers, if it's something browsers could work on without standards groups, or if there are already proposals in standards groups that are in the works (here’s a great example of that in action over on the [Web We Want GitHub repository](https://github.com/WebWeWant/webwewant.fyi/issues/37). 

A great example of something that's already being worked on is the HTML Controls submission (and there were actually a few other submissions on HTML Controls as well). There is a standards initiative called [Open UI](https://open-ui.org/) that's working toward making controls more customizable and extensible, starting with `<select>`. Even though this problem space is being worked on, the submissions here are still important as it provides additional evidence that browsers are working on fixing the right problems. 

## The Web We Want In The Time Of COVID

For the moment, our in-person sessions are on hold, but we're looking into ways to keep the community engaged and active in this intiative so stay tuned for developments there. 

We're still taking submissions to the Web We Want, so if you have a problem or feature gap in the web platform, let us know and submit issues on the [Web We Want website](https://webwewant.fyi/) or [upvote submissions](https://webwewant.fyi/wants/). Issues are now being tracked in GitHub in an attempt to allow more engagement and discussion from the community and browser and standards folks. There is no want too small or too big, so let us know and help to move the web platform forward!