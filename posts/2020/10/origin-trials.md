---
title: What the heck is an Origin Trial?
description: Diving into another way developers can experiment with and provide feedback on upcoming Web Plaform Features 
date: 2020-10-28
tags:
  - web platform
  - origin trials
layout: layouts/post.njk
permalink: posts/2020/10/what-the-heck-origin-trials/index.html
---

<p class="blog-post__date">28 October 2020</p>

My role of the Edge Developer Experiences Ecosystem team tends to revolve around gathering developer feedback. I run an initative called [The Web We Want](https://webwewant.fyi), I setup a new UserVoice page for Edge specific feedback (which I won't link to as it's being deprecated and replaced), and I pay attention to what gets tweeted to me and make sure to tag the right folks so that feedback gets filed. Nevermind all the other places I'm looking: in Standards group forums, Slack groups, blog comments. 

There's a lot of places to leave feedback, and when I think about the type of feedback I'm focused on gathering, it's about things that don't have an implementation or solution yet. 

Which leads me to browser Origin Trials. 

## What's a browser Origin Trial?

Origin Trials are a way for developers to test and use experimental web platform features for a limited amount of time in exchange for feedback. Feedback is key in origin trials as browsers are granting developers access to ensure that the feature makes sense and is usable. It's an iterative and open process and allows the engineers building the platform feature a chance to incorporate feedback and make changes to the feature. 

So often in the past, web platform features were developed without input and this offers developers anywhere a chance to try out some new bleeding edge web tech and provide feedback on how it works. 

## How do I use an Origin Trial?

[Microsoft Edge](https://developer.microsoft.com/en-us/microsoft-edge/origin-trials/) and [Google Chrome](https://developers.chrome.com/origintrials/#/trials/active) both offer Origin Trials for developers. 

At this particular moment you might be thinking, wait, Edge and Chrome both have Origin Trials? Aren't they both Chromium browsers? Will the Origin Trials be the same? 

And the answers to that are yes, yes, and no. 

The Origin Trial program launched back in May during Build for Microsoft Edge and we have platform features, like web primitives for dual screen devices, that our team would be working on and not Chrome. So the sets are different.


### Origin Trial Process

To get started developers should find an Origin Trial they're interested in experimenting with and register for it. You'll register the origin you want to use the experimental feature on and you'll be issued a token.

You'll then have to add some code to your website one of two ways to use the token provided to you.

Option 1: Using a <meta> Tag

`<meta http-equiv="origin-trial" content="your-token-gues-here">`

Option 2: Add Origin-Trial to your HTTP server response headers, example:

`Origin-Trial: your-token-goes-here`

And that will activate your origin trial. There are some more guidelines about allowed origins, subdomains, URL paths and query params in the [Edge Origin Trial Documentation](https://docs.microsoft.com/en-us/microsoft-edge/origin-trials/) as well as a walkthrough on how to register or unregister an origin trial. Chrome also has a [getting started guide](https://web.dev/origin-trials/) for their origin trials though the process should be the same.

### Submitting feedback and trial expiration

At their core, origin trials are provided so developers can try out new APIs before they are shipped and provide feedback about the experience of using the API and browser vendors can then assess and incorporate that feedback if they decide to do so. 

These features are not necessarily complete when they're in an origin trial and may or may not be available in other browsers so trials are time-boxed to 6 weeks for two reasons: 

- If developers would like to continue to utlize the trial they have to provide feedback at the end of the 6 weeks. Again, feedback is key so renewal of the origin trial is based on providing feedback. 
- This prevents developers from baking is not complete or may need to be revised heavily.

Even if an origin trial is successful, the API will have a period between the end of the origin trial and the feature landing where it will not be available to developers. Most likely there will be improvements to be made before the feature lands.

### Provide a fallback

Origin trials offer a chance to use some cutting edge web platform technology on your website, because of the nature of this kind of tech, the feature may or may not be available in other browsers so always provide a fallback so that your experience doesn't break for your customers who may be using different browsers. 

You should provide a fallback anyway due to the limited duration of an origin trial. Maybe you try out a feature and realize it's not what you need. 

## The edge of the web (no pun intended)

Origin trials provide a unique opportunity to flip on an experimental feature for all the visitor's to an origin. No one has to turn on any experimental flags to get a feature to work, it just *works* (again, for a limited time). And it provides a chance for developers to provide critical feedback to API authors. 

As I've immersed myself further into the world of the web platform, one constant I seem to hear is that developers want to know what browser vendors / API authors are doing. They don't want these things developed behind closed doors and they want to be able to provide feedback. 

Well that moment is here. There are a multitude of ways to get involved, but origin trials provide a very hands on way to do so. 

Personally, I'd want to go try out the [dual-screen and foldable device primitives](https://developer.microsoft.com/en-us/microsoft-edge/origin-trials/dual-screen-and-foldable-devices-css-and/registration/) available in Edge. As someone with a background in design, the idea of getting to tinker with these CSS and JavaScript primitives to provide an enhanced experience for those on dual-screen devices is exciting.  

So go explore! See if there's something experimental Chrome or Edge is working on that you can use and give it a whirl. Be involved in moving the platform forward with us.
