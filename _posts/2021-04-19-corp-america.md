---
layout: post
title: The World of Corporate America, April 2021
slug: corporate-america-april2021
tags: [posts]
author: Florian
---

This is a follow up to my previous post [here](https://floverfelt.org/posts/corporate-america-february2021).

Honestly, not much has changed. I'm once again bored at work and feel fairly ignored, so I'm writing a blog post about what's taken place since I previously wrote about corporate America.

## March

I became (and still am to a lesser degree), extremely frustrated by my work situation. As one of the most junior people on my current team, I was asked to move to a different team over the heads over much older, more veteran engineers because the other engineers "didn't want to do it." Apparently working at work is optional.

Come to find out, the new team, Link, needed me to develop a feature that integrates with a third team, PHL. I've never interacted with the PHL team before and despite Link having 3+ more qualified engineers available to do this, I got asked to do it.

As I quickly learn, PHL does *not* want this feature. They repeatedly ghosted us on chat, refused to show us their code base, and never once thanked us or even showed interest in **the feature that they requested**. Finally, when we did release the feature that was apparently so important I had to be yanked away from all other work to do, PHL asked us to revert it because it would be too much work for them to test it.

Utterly bizzarre.

I complained extensively to my manager about the ridiculous expectations of the situation (my previous team was also still expecting me to do work for them at the time). This year I got promoted to Senior Engineer during our review cycle. Nobody cared, but I got a nice pay bump.

## April

I was then asked to do another integration where we essentially add additional fields to an API request/response chain that happens.

The lead engineer on the Link team then pretty much did it all himself. 

This makes sense, I guess, but also, why did you ask me to do it?

At this point, everybody has basically forgotten me and I'm just sitting quietly and collecting a paycheck.

## Things I've learned

I do feel like I've learned a lot these past few months, but none of it is all that encouraging.

#### College is a lot more "the real world" than the real world

I remember at UVa a lot of older men (mostly) talking about how once you enter "the real world" you'll have to really work and yada yada yada...

This is completely untrue and, if anything, college was a *much* more accurate representation of my knowledge and work ethic than the "reality" of corporate America.

First, it's basically impossible to get fired at a sufficiently large company. I'm not talking about a general layoff where they cut some random 10% of engineers or product managers or whatever. I'm talking about a legitamete firing due to work ethic and non performance. This is what has to happen:

1. You have to be so un-likeable that people don't want to be around you. If you're nice enough and pleasant to be around, this whole chain stops pretty quickly.
2. You have to just straight up *not* do any work with no excuses.
3. Your manager has to *want* to fire you. Managers hate firing people. Even if their reports are terrible employees, no manager wants to fire anybody.
4. You're then required to be put on a probationary period of three months. The manager must also *want* to design and keep up this program.
5. Hiring takes anywhere from one to six months, so the manager must also be willing to pick up the persons work or delegate that person's work for the time it takes them to be replaced.

This is all an (apparently) monumental task and the bar is so low that doing basically anything at any step in this process prevents you from being fired.

One person on my team spent over a month before even *asking for help* on a ticket that was assigned to him. He's been chronically under-performing and he fails to make even the most basic of code changes. *And* he's been doing this for over a year.

But he's being given a fresh start this year because somebody deemed that he just "wasn't interested" in the tech stack we assigned him. Although, he himself never said this.

If this were a college environment, and the same person was given an end-of-semester test, they would fail. They would not get credit. We wouldn't talk about how they were depressed, or they just weren't interested in the subject, or whatever, you'd just fail. Of course, most classes were transparent and set your expectations clearly, unlike at companies where...

#### There's basically zero expectations

When I joined the Link team, nobody said anything resembling "This is the work we're expecting you to do, these are the deadlines, this is why we requested you, etc." Instead, I literally just got dropped into the stand-up and was expected to...? What?

Pick up new tickets? Create tickets that I thought needed doing? Only do Java work, which is what I was brought there to do? I had to setup multiple meetings where I had to *ask* what other people what they wanted me to do. Which begs the question, if nobody wants me there, why was I asked to be there?

Is it too much to ask that somebody else do their job and assign me work or at least set up a meeting and tell me what they are trying to achieve? I guess so?

Software Engineering (at least at my company) operates in this weird space where the two people primarily assigning and tracking your work (Project Managers & Scrum masters) have no clue how programming works or how long it takes to do certain tasks. This means you can basically say anything as an excuse and nobody seems to challenge it because what do they know?

All in all, this pretty much just leads to a vacuum of authority and accountability where you can pretty safely get away with spending a month or more adding log statements to code.

#### Other things that happened

- The application is a 10k + LOC Java app. The product manager had no idea what language the app she's been managing is written in and when asked to name the developers who knew Java, she named two of the four people on our team who specialize in it.
- The app had consistently been spitting a massive ERROR message on boot. It wouldn't interrupt the boot process but it was incredibly ugly and looked bad. I fixed it in 30 minutes and nobody cared.
- Upon suggesting that we incrementally switch Spring's autowiring to the way *the developers of Spring recommend we do it* I was told we needed to have a "team discussion to reach an agreement" and it was swept under the rug.
- I raised multiple pull requests that took anywhere from 3 to 5 days to review.
- When asked to review my code, I was either ignored during our daily meeting or yelled at for asking somebody to "context switch" from the work they were doing.
- I recieved a lot of passive aggressive feedback on my code implying that I should have known something I didn't. Or just straight up adding some new requirement. Nobody seemed to acknowledge that I'd been around for less than a month.
- I was chastised for suggesting that something needed to be documented. When I asked where the documentation was, they pointed to the revision history of a ticket that had been closed 3 months ago by a developer who'd since quit.
- Multiple QA team members did not know how code reached dev/qa/stage. They would frequently ping me before a PR had been merged and asked me if it was in QA yet.
- We frequently had hour or more long "parking lot" meetings which were "optional" and yet that's where we decided everything that took place in the app. Instead of documenting things, we did this instead.
- The Scrum master asked that everybody turn their cameras on one day and nobody did. This was just very awkward.

#### Summation

All in all, I've treated the last few months like being a consultant on a short term project. I stopped asking for work unless it was explicitly assigned to me and did not raise any more issues or feedback after the (disastrous) first few weeks on the project.

I don't like working this way and I think it was wrong but necessary to do in this situation. The situation felt dehumanizing and my actions were in opposition to my values. This was probably why I was/am so frustrated with it all.

