---
layout: post
title: When is Software Good Enough?
slug: software-good-enough
tags: [posts, software, programming]
author: Florian
---

I had one of the most pleasant software experiences a few months ago. On the DMV's website. I was renewing my van's registration and the DMV website had a very basic HTML form for CC details, address info, etc. and a page or so long explanation of how renewing a registration works.

When you submit the form, you get an email, and you're done. This is great! And none of this technology is new.

This got me wondering...

## When is Software Good Enough?

This post may turn into an amalgamation of miscellaneous thoughts around software, but nevertheless.

[Jaron Lanier](https://en.wikipedia.org/wiki/Jaron_Lanier) said something I found pretty compelling in "[You Are Not a Gadget](https://en.wikipedia.org/wiki/Jaron_Lanier#You_Are_Not_a_Gadget_(2010))." It amounted to, roughly:

```
We think of software as this simple thing that will solve every problem, but as soon as it's implemented it grows into an unworkable mess.
```

We're basically stuck in this loop where we think "Oh, let me develop a software solution to fix this simple problem," and then the solution explodes in complexity beyond the scope of the original problem.

We don't really seem to learn from this either. We just keep designing and building products that do this.

Given how much Software Engineers fetishize simplicity, we are terribly bad at implementing it. For example, while on the Link team at work, we were building out a Spring boot app.

The ask for the app was to forward messages from a frontend Salesforce (SF) application to a backend [Mirth](https://www.mirthcorp.com/community/issues/browse/MIRTH/?selectedTab=com.atlassian.jira.jira-projects-plugin:summary-panel) processor. We'd consume the message from Salesforce, log it, and then send it to Mirth.

Perfectly reasonable and doable, but also completely pointless. Why doesn't the SF app just send the message directly to the processor? Who knows?

All the app did was stuff like this -- shuttling data between applications that could easily just *send it themselves*. Partly, this is a tale of corporate shenanigans: Somebody somewhere on an org chart decided that the priorities were such that ... we need a totally seperate app for this.

But it's also partly the fault of the Software Engineer(s). Building a new app is fun! Why wouldn't you want to do this?

I guess the point of this post is to ask yourself this about new software -- when will it be good enough? If the answer is "never," then perhaps steer clear.

## Some Caveats

Obvious caveat: I'm not referring to maintenance, new legitimate feature requests from users, etc. These are valid reasons to expand a piece of software. I'm referring to software companies that literally seem to do nothing except build out things that nobody ever wants in the name of infinite growth & engagement. Some examples:

- Venmo requiring you to use emoji's instead of plain-text. 
- 90% of the features offered by Facebook. 
- Reddit's award system.

Solve the core business/human value of the software and move on. 

Second caveat: Following this advice will probably not make you wildly wealthy. Investors like the idea of these mega-apps that grow forever and lose money to become the next big thing.

Final caveat: I'm not against new software! [Coinbase](https://www.coinbase.com/) solves a legitimate need in a new space with minimal bloat. It's totally fine! [Robinhood](https://robinhood.com/us/en/) is the same way. Software companies can be great and so can software, just ask: When will it be good enough?