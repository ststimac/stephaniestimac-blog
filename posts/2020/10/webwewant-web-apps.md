---
title: Web We Want Web Apps Survey Results
description: The intial results from a validation survey on the Web App submissions to Web We Want
date: 2020-10-05
tags:
  - web we want
  - standards
layout: layouts/post.njk
permalink: posts/2020/10/webwewant-web-apps/index.html
---


I&#39;ve started to run initial validation surveys on Web We Want submissions to help determine which of the submissions are worth continuing to investigate. Note that despite some of the scores being negative, this doesn&#39;t necessarily mean the submission is invalidated, taking into account the answer to the &quot;what is the reason for your score&quot; helped gain more insight into what affected respondents scores.

For the Web Apps category, there were 7 submissions to the Web We Want as of the time I conducted this survey.

## Survey Details
There were 50 respondents to the Web Apps survey, promotion being driven only through Twitter.

- 27 front-end developers
- 1 back-end developer
- 21 full-stack developers
- 1 Other

These are the 7 submissions to the Web We Want for Web Apps that the survey centered around:

- [I want global keyboard shortcut event listeners](https://webwewant.fyi/wants/110/)
- [I want web apps to be able to work in other contexts (like car displays)](https://webwewant.fyi/wants/103/)
- [I want to allow PWAs to be able to request permission to bypass the same-origin policy after install](https://webwewant.fyi/wants/101/)
- [I want to enable extensions to run as PWAs](https://webwewant.fyi/wants/100/)
- [I want web apps with elevated privileges to be vetted](https://webwewant.fyi/wants/89/)
- [I want limited reactivity in the DOM/Web Components](https://webwewant.fyi/wants/33/)
- [I want a way to build desktop/mobile/web apps with one codebase and have it run everywhere](https://webwewant.fyi/wants/31/)

## Survey Questions

The survey asked respondents to rate the usefulness of each Want on a scale of 0-10, using NPS, with 0 being &quot;Not useful at all&quot; and 10 being &quot;extremely useful.&quot; Respondents were then asked to pick their top 3 Web App Wants from the list. This survey also added an additional optional question for respondents to provide a reason why they chose the score they did for a feature.

## Web App Wants

### I want global keyboard shortcut event listeners

**NPS Score** : -28
9 promoters | 18 passives | 23 detractors |


![NPS Score for global keyboard shortcut event listeners: -28. 9 promoters, 18 passives, 23 detractors](/img/www-webapps-survey/keyboard-shortcuts.png)

#### Verbatims: what is the reason for your score?

> &quot;This is an area where web apps fall short of native apps. I&#39;d love to see the situation improved to bring feature parity. That said, there are real concerns about shortcut handling here. At minimum, this should only be allowed for installed apps, it should be limited to using some well-known shortcut prefix (CTRL, Shift, Option, Windows key, etc.).&quot;

> &quot;Enhanced keyboard accessibility. As alluded to in the proposal, privacy concerns would need to be addressed&quot;

> &quot;I see it useful but also the security risks are great. If it&#39;s implemented then protections should be put in place i.e. if there&#39;s a form with a password field (\&lt;input type=password ) or some other known identifier than the feature should be disabled. As for OS wide, well not sure how you protect against that. That said, it isn&#39;t hard to write an app which logs keystrokes and embedded it within a program.&quot;

> &quot;would cut down on cross-OS boilerplate for things like copy paste close save etc.&quot;

> &quot;This brings the web closer to native app parity. It sounds like a Fugu API&quot;

> &quot;Web apps are moving to touch and click interfaces, not to keyboard interactions&quot;

> &quot;Would make it a lot easier to develop web apps as you&#39;ll not need to write code to recognize shortcuts for different operating systems&quot;

> &quot;we currently have our own hand rolled solution which works well but it&#39;s difficult to manage which shortcuts are active and when given the different elements that pop up on screen at different times. Particularly when the event listeners need to attach to window and not the DOM node that they belong to.&quot;

> &quot;A neat idea, but can be easily abused. For example, it could also enable online keyloggers that don&#39;t require installing malware, making it extremely difficult for anti-virus software to detect.&quot;

> &quot;Allows us to develop enterprise-grade PWAs that work well in desktop environments&quot;

> &quot;I&#39;m concerned about security, but global keyboard listeners would be extremely helpful for productivity and professional software. All the Ops teams I&#39;ve worked with, for instance, have to switch between multiple web apps and dashboards, and alt-tabbing is the most efficient way to do that. If they were able to set up shortcuts for commons tasks, that would be a game changer.&quot;

When reviewing the &#39;reason for ratings&#39; responses, there does seem to be a desire for this feature but there are clear concerns about privacy and ensuring a feature like this wouldn&#39;t be abused. This seems to be the reason for the low score.

### I want web apps to be able to work in other contexts (like car displays)


NPS Score : -4 
15 promoters | 18 passives | 17 detractors

![NPS Score for web apps being able to work in other contexts like car displays: -4. 15 promoters, 18 passives, 17 detractors](/img/www-webapps-survey/car-displays.png)

#### Verbatims: what is the reason for your score?

> &quot;Working in the automotive industry, I can see how this might be appealing. Don&#39;t think we need a media query since current media/feature queries seem sufficient but access to certain APIs/data from a vehicle would open up the possibility to build a variety of features into a web app.&quot;

> &quot;That&#39;s a great idea, it&#39;ll enable all sorts of integration that&#39;s restricted at the moment.&quot;

> &quot;Actual rendering of a web app probably isn&#39;t what we need in Android Auto. It&#39;d be great to get more Electron -\&gt; Car APIs so that apps like Slack/Teams can work in-car, but full rendering...no&quot;

> &quot;Microfrontends are one of my best bids for future web apps, used in any kind of interface (vending machines, smartwatches, refrigerators...)&quot;

> &quot;If you put the web onto car displays people will actually die. You have no control over whether something is appropriate for the car or not and blindly trusting web developers when they tell you it is is dangerous.&quot;

> &quot;I like the general idea of contexts that help to define a more accessible UI, however more generalized (&quot;low-distraction&quot; vs &quot;car display&quot;)&quot;

> &quot;Mini apps in China are targeting cars etc., so Web should, too.&quot;

> &quot;This would make everything much more accessible to a wide range of developers.&quot;

### I want to allow PWAs to be able to request permission to bypass the same-origin policy after install

**NPS Score** : -38 
11 promoters | 9 passives | 30 detractors 

![NPS Score for allowing PWAs to be able to request permission to bypass the same-origin policy after install: -38. 11 promoters, 9 passives, 30 detractors](/img/www-webapps-survey/same-origin.png)

> &quot;Useful but I do have privacy concerns about this.&quot;

> &quot;I don&#39;t like the idea of major functionality only being enabled after the app is installed. This seems a better fit for Electron.&quot;

> &quot;Feels like the natural growth of PWA&#39;s to get respected as full applications.&quot;

> &quot;the permissions model is interesting but would people use it effectively? is there maybe another, better solution?&quot;

> &quot;This is by design for security. Not a good idea&quot;

> &quot;not sure about the security implications and how to communicate the consequences of the decision to the user&quot;

> &quot;Not sure the security implications are worth it. Should we be able to do everything in the browser? I would think an separate PWA-only API provided by the browser would be better.&quot;

> &quot;I see the appeal, but I&#39;m scare it would get out of control. Shady businesses like Facebook would absolutely abuse that power for profit.&quot;

There is interest in this, but abuse and privacy concerns driving the overall score down.

### I want to enable extensions to run as PWAs

**NPS Score** : -66 
4 promoters | 9 passives | 37 detractors 

![NPS Score for enabling extensions to run as PWAs: -66. 4 promoters, 9 passives, 37 detractors](/img/www-webapps-survey/extensions-pwas.png)

#### Verbatims: what is the reason for your score?

&quot;Better solved with web packaging&quot;

&quot;Extensions should have access to the same APIs that PWAs have access to.&quot;

&quot;While I agree the security concerns are important, this doesn&#39;t feel like the right way to tackle the problem&quot;

&quot;for this browser extensions need to be standardized first, otherwise an API like this would harm the open web (at least from what I understand)&quot;

&quot;I don&#39;t see the use case.&quot;

&quot;Not sure how this would be used.&quot;


### I want web apps with elevated privileges to be vetted

**NPS Score** : -50 
9 promoters | 7 passives | 34 detractors 

![NPS Score for vetting web apps with elevated privileges: -50. 9 promoters, 7 passives, 34 detractors](/img/www-webapps-survey/elevated-privileges.png)

#### Verbatims: what is the reason for your score?

> &quot;The web is supposed to be decentralized, and I don&#39;t support any feature that centralizes authority.&quot;

> &quot;While vetting is good, that&#39;s just another way to put up a paywall and create a store. With the previous proposal to bypass same-site origin the OS could expose API&#39;s that the PWA can access to do the necessary calls.&quot;

> &quot;I&#39;m not sure I want centralized authorities here&quot;

> &quot;Seems sensible, but users should be able to give those permissions out, rather than be vetted. It&#39;s not a &quot;web&quot; thing&quot;

> &quot;No, the web should remain open for all&quot;

> &quot;Google Play has IMO been a complete failure on this front. Even with the resources Apple has sunk into the AppStore, it&#39;s vetting has had a checkered past. This feature would give nothing more than an illusion of security.&quot;

> &quot;This would make some problems like permission prompts go away, but who should be the authority that vets?&quot;

> &quot;That would be very difficult to implement. As long as non-vetted apps are still able to access the same functionality as vetted apps, I guess it would be okay.&quot;

### I want limited reactivity in the DOM/Web Components

**NPS Score** : -2 
19 promoters | 11 passives | 20 detractors

![NPS Score for limited reactivity in the DOM/Web Components: -2. 19 promoters, 11 passives, 20 detractors](/img/www-webapps-survey/dom-web-components.png)

#### Verbatims: what is the reason for your score?

> &quot;Having a standards-based way to make the way more reactive will cut down on the variety of frameworks we need to learn (reducing the barrier to entry into the industry) as well as contribute to performance benefits as we don&#39;t need to load third-party frameworks for basic FE/BE interactions.&quot;

> &quot;This is a must, we&#39;re tired of using libraries that change every now and then, always for the same&quot;

> &quot;The less we rely on libraries, the more we all benefit.&quot;

> &quot;Anything that improves developer-friendliness without the need for heavy-weight frameworks&quot;

> &quot;While it sounds nice, I personally use Blazor these days which gives me effectively the same results. Might be nice but it would be good to work with the web components teams to figure out there minimum needs. i.e. fast.design&quot;

> &quot;Why not just let the community libraries fill this gap? Feels like a complex problem that can only be solved in a limited fashion&quot;

### I want a way to build desktop/mobile/web apps with one codebase and have it run everywhere

**NPS Score** : 46 
33 promoters | 7 passives | 10 detractors

![NPS Score for having a way to build desktop/mobile/web apps with one codebase and have it run everywhere: 46. 33 promoters, 7 passives, 10 detractors](/img/www-webapps-survey/one-codebase.png)

#### Verbatims: what is the reason for your score?

> &quot;The answer isn&#39;t changing the web platform, but allowing PWAs to run everywhere and be listed in app stores.&quot;

> &quot;I think this is a developer problem, not a problem with the web. Sure, there are a few features missing on the web platform, but being able to use the same codebase across multiple devices isn&#39;t one of them.&quot;

> &quot;I believe the prevalence of Electron has shown that this is something that&#39;s super useful.&quot;

> &quot;I would build for many more platforms if this were possible&quot;

> &quot;Very useful. Enterprises want a way of pushing PWAs easily to users devices.&quot;

> &quot;The phrase &quot;write once run everywhere&quot; may have been popularized by Java, but it has been tried hundreds of times. C++, Python, Perl, Java, all have multiple attempts, not to mention Go, Dart, Kotlin, etc. None have achieved any significant dominance. Let&#39;s use browser developers time wisely.&quot;

> &quot;The old dream of write once, run everywhere.&quot;

## Pick Your Top 3 Wants for Web Apps

1. I want a way to build desktop/mobile/web apps with one codebase and have it run everywhere
2. I want web apps to be able to work in other contexts (like car displays)
3. I want limited reactivity in the DOM/Web Components

![A chart showing the ranking of the top 3 wants people picked for Web Apps](/img/www-webapps-survey/top-3.png)

## Conclusion

After running this initial survey, the Microsoft Edge Web Apps team is looking into potentially investigating 5 out of the 7 Wants submitted.  

If there’s something you want for the Web Platform or Developer Tools, head to [The Web We Want](https://webwewant.fyi) to submit your proposal. It could end up in the browser or browser DevTools! Like the [DevTools Source Order Viewer](https://blogs.windows.com/msedgedev/2020/09/15/source-order-viewer-edge-devtools/), which was submitted last year to the Web We Want and is now available in the Edge and Chrome Developer Tools in the Canary channel.  