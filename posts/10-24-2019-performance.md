---
title: Location, Privilege and Performant Websites
description: A post on performance and assumptions made due to location
date: 2019-10-30
tags:
  - performance
  - privilege
layout: layouts/post.njk
---

<p class="blog-post__date">30 October 2019</p>

I would say that I live an extremely privileged and comfortable life. The privilege from having a good paying career in a large tech company opened up the opportunity to purchase a home, on much more land than you’d get in the city, 30 miles outside of downtown Seattle. 

Though to some friends it feels as though I’m really far outside the city, I’m technically a part of the Seattle Metropolitan Area and despite being in a rural area, I’m close enough to Redmond and Bellevue that something like mobile phone and data coverage shouldn’t be an issue. 

These two things were not things I really paid attention to while looking for a home unless the property was so far out that there was no coverage at all. I figured once the internet was installed, I wouldn’t have to worry about spotty coverage. I would have WiFi and it would be fine. 

## An Unreliable Network

I was later proved wrong though, about not having to worry about data and cell coverage; the power went out and with it, internet connectivity. Wind storms and even a hard rain can knock the power out where I live and in the winter it’s a somewhat common occurrence. For the most part, power is restored within an hour or two, but there have been a few severe wind storms and one was so severe last February that the wind woke me up at 2:30 AM. 

While I ran upstairs to try and assess what was happening outside with branches snapping and loud booms of trees falling in the distance, I attempted to reach the Puget Sound Energy website on my mobile browser to report the outage. 

I refreshed the page multiple times while my phone said I had data coverage and was on the network (one, maybe two bars at times), but the PSE page came up as offline. I finally managed to get the page to load to report the outage after about 5 minutes. 

In the morning, the power was still out and it was clear this has been a devastating wind storm. Electrical fires were being started by downed power lines, trees were blocking two out of three exits out of the neighborhood.  

Since I didn’t have a generator for my home, I was without power and internet for nearly 24 hours. Many updates were being posted to Facebook and Twitter but those struggled to load just as the PSE Outage listing page did. I couldn’t access the information I needed about repairs or status of the repairs. It was frustrating and isolating. 


## Unused JavaScript

After the storm, I was determined to find out why the 'Report An Outage' page was so painful to download.

I profiled the PSE Outage page after [Addy Osmani tweeted](https://twitter.com/addyosmani/status/1085439006433669120) about using the Coverage panel in the DevTools to check how much unused JavaScript was being loaded.

![alt: Edge DevTools Coverage Panel](../../img/post-4/coverage-panel.png)

There were 4.6MB of unused code being downloaded on a page whose main and only content, apart from a sign in button, is a form to submit your address.

![alt: webhint.io performance budget hint](../../img/post-4/webhint-perf-budget.png)

According to [webhint's Performance Budget hint](https://webhint.io/docs/user-guide/hints/hint-performance-budget/), on a 4G network, it will take a staggering 55.3s to load all the resources.

The results from [web.dev](https://web.dev/) aren't great either. Performance as a category got a zero.  

![alt: https://web.dev screenshot showing 0 performance score](../../img/post-4/webdev-analysis.png)

I personally don’t have to worry about how much data I’m using to load web pages on my phone but that doesn’t mean I want to spend time waiting for megabytes of unused code to slow down my access to a website, especially when I can’t access a WiFi point. 

On the other end, there are people who have to worry about how much data they use. Trying to simply report an outage or get an update on when power could be restored should not cause additional anxiety in a situation. Whether it’s anxiety about a lack of access to information or anxiety about how much their phone bill is going to be because of how much it took to load a page whose size could be reduced immensely if developers took a little more care to assess what it is they’re serving to their customers.

It’s also worth noting that in trying to serve all that extra JavaScript, your phone is working harder and the battery will drain quicker, which normally wouldn’t be such an issue but when you don’t have power in a storm or natural disaster, that becomes a concerning situation.

## Privilege in Code

Unconscious privilege hides in delivering so much unused code to customers. In not taking the time to understand what the implications are of using the code you choose to use and how large those files are, we assume that all of our customers are in the same situation with the same access to resources.

NPR smartly chose to build a [text-only](https://text.npr.org/) website so that people with limited internet connectivity during Hurricane Irma could receive up-to-date news.

If you do assess your code and for whatever reasons find that you cannot reduce the size of your website, be it time or staffing propose adding a text-only website, especially if you provide a service that is essential to most of the population in your area.

Your text only website doesn’t need to be a text-only version of every single piece of content on the site either. Figure out what the essential pieces your customers need access to are and build it with plain, semantic HTML.
Personally, when I’m in a situation where I don’t have power due to a weather event, I’m not concerned about what your website looks like. I don’t care about the branding or interactivity or being delighted. I care about information and whether I have been given an option to find what I need easily and without hindrance.

## A Web for All

Assuming all of your customers are living the same life, with the same privilege, with the same access to fast internet and data is the quickest way to ensure you’re excluding some of them and not providing the same level of service the rest get. It’s most likely not even happening intentionally, bias is inherent in us all in some way or another. Bias based on location is something I hadn’t considered before my experience on a subpar network due to where I live. 

But if you’re providing a service or utility that is essential to a large portion of your community, it’s important to take a step back and assess your user experience from a different perspective. 

One might assume that because Seattle is a booming tech area, we should all have access to fast internet and top of the line devices. But this isn’t the case, and Seattle is not in fact full of people in tech living privileged lives due to their salaries. Many don’t live in Seattle, or even Bellevue proper due to the cost of living and when your customer base spans urban to extremely rural, you need to ensure your rural customers have the same access as the urban ones. 

In Unincorporated King County, where I live, the 2018 [census estimate for population was 247,240](https://www.kingcounty.gov/~/media/depts/executive/performance-strategy-budget/regional-planning/Demographics/Dec-2018-Update/UKC_profile_2018.ashx?la=en) (PDF). King County is only one of many counties that Puget Sound Energy serves with a customer base of 1.1 million. If everyone in this demographic had PSE as their electricity provider, that’s 22% of customers who live in a suburban to rural setting. That’s 1 in 5 people. Similarly, [according to the United States Census Bureau](https://www.census.gov/library/stories/2017/08/rural-america.html), 60 million Americans, that is 1 in 5, live in rural areas. To ignore the needs of 20% of the population is egregious.

Testing on a <$100 Android device on a 3G network should be an integral part of testing your website. Not everyone is on a brand-new device or upgrades often, especially with the price point of a high-end phones these days.

When we design and build our websites with the outliers in mind, whether it’s for performance or even user experience, we build an experience that can be easy for all to access and use — and that’s what the web is about, access and information for all.
