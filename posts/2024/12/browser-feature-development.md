---
title: "You can pay for that: How web browser features get built"
description: A guide on all the different ways web platform features, APIs, etc in web browsers can be built.
date: 2024-12-06
tags:
  - web platform
  - browser development
layout: layouts/post.njk
images:
    thumb: /img/2024/browser-features.webp
permalink: posts/2024/12/how-browser-features-are-built/index.html
---

As I have spent the last 6 months starting to explore the rather precarious position we've placed web ecosystem in, with regard to how browsers are maintained and funded, I thought I'd dive into another angle: The ways that web platform features get prioritized and built. 

I worked on Microsoft Edge, so I have direct experience working on a browser team. My current work is at [Igalia](https://www.igalia.com/), which is an open source consultancy that is hired by companies to work on many things across technology. My team, the web platform team, implements web platform features and APIs, and works on their specifications. Yes. You can pay for browser features to be built and for specifications to be written/updated/continued. We'll talk about both.

## Browser vendors 
Browser vendors are the companies that develop, maintain and distribute a web browser. _Some_ browser vendors are also stewards of a whole engine/browser (blink, WebKit and gecko). Google, Apple, Mozilla, Microsoft, Opera, Vivaldi, etc are all browser vendors. Google, Apple and Mozilla are engine stewards.

There are *many* teams that make up an entire browser team. A browser is so much more than just the web platform too. There is quite a lot of thought and design that goes into even the smallest user experience updates. 

General consumer facing features, which typically have a UI component, tend to often get prioritized over more "hidden" web platform features for developers. The general consumer base is larger than the developer base. The goal is more market share (more people using your browser) which helps bring money to the browser vendor. 

The web platform team works on browser features and specifications and making sure the implementation matches the spec, so you don't get different behavior in different browsers. But they're also there to enable what we'll refer to as "first party" needs. 


### First Party Development
First party refers to groups within the same company as the browser vendor. Microsoft Office/Microsoft 365 is an example of a first party within Microsoft with web platform needs. Subsequently, their needs for the web will get prioritized. 

Surface Duo is another example. I spent a lot of time talking about the web platform primitives and design considerations for dual screen devices. Having layout capabilities that adapted to this new form factor was incredibly important so the specification and implementing those features were also prioritized.

In my experience, first party development is typically prioritized above all else as you're enabling/enhancing another product in the company. Especially if those products are money-makers. These are also broader company strategic initiatives and very visible ways to make impact. 

Come yearly review time, these things matter for compensation and bonuses. It is all deeply intertwined in company politics. These are things that make the company money and make the business case for having a browser. Bill Gates' [_The Internet Tidal Wave_ memo](https://lettersofnote.com/2011/07/22/the-internet-tidal-wave/) from 1995 even points out how access to the internet through PCs is vital for the business. Enhancing user experience and moving the web forward will be what wins consumers over.


## External Companies and Third Party Development 

Another scenario is when an external, or third party, company has needs for the web platform. My experience with this while working at a browser vendor company is more limited. Third party can also mean general web developers. It was much harder to get the needs of the general web development community prioritized when first party often takes priority. 

I truthfully can't remember whether it was/is possible for third parties to ask Microsoft to work on enabling certain features. I mean, of course you can ask, but I'm not sure how often an agreement would be made. With a relatively small team working on enabling web platform features, this probably wasn't/isn't a common scenario unless there's some big underlying strategic initiative that would benefit the browser and company. This type of contract could entirely have been outside my sphere of work. 

The trouble with being a third party is that it's not as easy to align priorities or business cases.  In fact, you might even be a competitor.  Regardless, since resources are finite, it's likely that it's difficult to convince vendors to pay attention to your specific needs.  At the end of the day, practically speaking, funding is required to advance features, fix bugs, etc.


## Consultancies 

Guess what? Yes! You can hire experts to implement web browser features and/or give you that attention and priority!  Do you need a new feature implemented or spec'd? A consultancy can help. Do you need bugs that are affecting your organization fixed? A consultancy can help. 

If you have a need for a web platform feature, there are consultancies available for hire to help write and edit the specifications, work with standards groups, write web platform tests and get that feature shipped (or ready to be shipped). 

I work for [Igalia](https://igalia.com), and you can hire us for many things across many technologies and areas including web platform development. 

In fact, we've been pivotal in moving forward a whole lot of things in the Web Platform, including features like CSS Grid, [`:has`](https://bkardell.com/blog/canihas.html), container queries, MathML, classes in JavaScript, scroll snap, `list-stlye-type: <string>`...the list does go on and on. We work on lots of specifications and implementations for the web platform.  

Instead of waiting or relying on a browser vendor to implement the features you need, which could potentially be years or even possibly never, you can hire experts like Igalia to do this work. 

### Why should I hire a consultancy to build web platform features?

The most obvious answer is: It works. We've helped a lot of happy customers do amazing things.

Aside from needing features more quickly, hiring a consultancy like Igalia has advantages. We are experts in these processes and the dynamics of working in standards bodies, and our strength comes from not only our technical expertise, but our ability to navigate between the three main browser vendors with web engines to ensure feature design is agreed upon. This is a lot of work and often times it can be slow because there are only a handful of people at browser vendor companies who are responsible for reviewing patches, proposed features, design documents, etc etc.  

Let's say you are a customer with a web platform need. You most likely have a backlog of work for your engineering team. There could be a few different scenarios that prevent you from internally prioritizing the web platform need: No one on the engineering team has the technical background for the type of work you need done, someone might have the technical background but not enough time to manage the entire process of spec writing, test writing and implementation, or maybe the team just doesn't have the capacity based on broader company priorities and product roadmaps. 

When you hire a consultancy to do this work, then your product engineering team can spend time on the product work and roadmap while we work on the spec, implementation and coordinating among browser vendors. This stuff takes a lot of time, because it's the nature of the work, and it's our area of expertise. 

### Funding specific features
There have also been instances where specific features have been funded by the community or donors, primarily driven by a *want* for better support and not by a business need, even though there most likely are business needs for such feature improvements out there somewhere. 

The [MathML](https://opencollective.com/mathml-core-support/updates/mathml-h1-report-2024) work Igalia has been doing is an example of that. Igalia also ran [an open prioritization](https://www.igalia.com/open-prioritization/index) experiment where the community collectively selected and funded a feature. 

Sometimes there are really vital features the web needs, but for whatever reason, they're not a priority. With that being said, if anyone's interested in helping to advance and improve SVG, [drop Igalia an email](https://www.igalia.com/contact/). We'd love to work on it. 

## Closing
I have encountered many people since starting at Igalia earlier this year, who didn't know you could hire someone to build a browser feature, or work on a specification, or fix browser bugs. You can even hire us to work on improving a novel web browser engine (say hello to [Servo](https://blogs.igalia.com/mrego/servo-revival-2023-2024/)), because you might need a web browser solution that is more lightweight than the major open source options. 

Or maybe you need a browser for your Extended Reality/Virtual Reality device. With 50% of Meta Quest users spending time in the browser, it would be a missed opportunity to not offer the same on your device. This is where we come in with [Wolvic](https://wolvic.com/en/). It's designed with browsing in XR in mind, and you don't have to build a browser from the ground up. 

There are so many benefits to hiring someone to work on The Web in whatever way you may need. It also means the web platform can advance more quickly (in browser timescales anyway) because more people outside of browser vendors are working on things. 

And that's good for the overall health of the web ecosystem. 

_Note: Thank you to my colleague [Brian Kardell](https://bkardell.com/) for reviewing & editing this post, which had been taking up a lot of space in my mind for a long while._