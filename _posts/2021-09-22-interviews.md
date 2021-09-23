---
layout: post
title: Tech interviews
slug: tech-interviews
tags: [posts, work, life]
author: Florian
---

I recently applied to and was rejected from a small-medium healthcare tech startup that does device medical ordering. It's definitely a [systemic problem](https://floverfelt.org/posts/some-thoughts-healthcare-tech) and not a real problem, but it's more real than what I do now so :man_shrugging:.

And yeah, hiring is pretty much as bad as people on [HackerNews](https://news.ycombinator.com/) are always saying it is.

To be clear, I don't want to be sour grapes about this! Everybody was pretty nice, the technical problem was challenging but interesting, and things were mostly clear from the start. It was not a bad interview, per-se, it's more that the process as a whole is so bananas that it's difficult to make it a *good* experience at all.

## Initial Thoughts

Here are some high level takeaways, in no particular order:

- At no point beyond the first 10 minutes did anybody ask me about my resume, this included my portfolio work.
- At no point did we walk through *their* product. It's always funny to me that engineers are expected to not care about the product and only the technical components, languages, frameworks, etc.
- During the technical interviews, it was completely unclear what I was being judged on. I asked after, and it was pretty much just "can you communicate." Which means ...?
- The architecture portion was on a problem everybody in the room was intimately familiar with except for me. This isn't necessarily a bad thing, but it did make me feel like an idiot since I was essentially trying to design a solution in 10 minutes, on a Google Doc that they'd obviously been thinking about for *months* if not years.
- All the responses from them were delayed. Most communication took ~1 week to get a response and then the final "yes"/"no" decision email they missed their own deadline in responding to.

All pretty normal interview shennanigans (sadly).

## Asymmetric Information

Literally, the entire interview process is so completely obfuscated between interviewer and interviewee that it's almost laughable.

I sat down to write this post and was going to say "The goal of an interview is..." but then I realized even the ground-level definition of *why* a company is hiring somebody is pretty opaque. 

Personally, I would say the goal is to find somebody who's knowledgeable in your field, responds in a timely way, and is generally pleasant and amicable to work with. This is pretty much how I would judge a candidate if I ran my own company, but *this is not necessarily how the employer thinks*. 

They could very easily be looking to hire engineers who know the in's and out's of Python and can work indepdently. They could be hiring knowing that they're pivoting to mobile and want to start pipelining people with that experience. They could be doing a hire largely looking to diversify their workforce. 

You really have no idea what they want, and the wild thing is *you have no way of knowing because you aren't in the company.*

The devil's advocate retort to this is "Well, you should just ask what/why/who they are hiring and clear up the information gap." The problem, here, is that you're almost definitely going to get a skewed response to that. Most managers are nice, they [don't really want to reject you or even fire you if they can help it](https://floverfelt.org/posts/corporate-america-april2021) and it bears re-iterating here - *you aren't in the company*. Things that are so apparent to the manager that they don't even mention are completely hidden from you.

This discrepency is frequently paraphrased as "giving the right answers" to interview questions and it's pretty apropos. In this most recent interview, I felt like I was guessing at their architecture and giving it a good first pass, but what the hell do I know? I have no idea the different ways they've tried modeling their data and the various pros and cons. But I can hardly say in an interview "Well, I feel like you guys would know the best way to solve this given that you've been working on it for weeks/months/years." Because then I'm not playing along with the game.

Likewise, you also have no idea *who the person you're interviewing with is*. There's a very good chance that they are also thinking about quitting their job and dislike it there or are looking for a change. Or worse in some ways, they could be completely clueless. 

We once did resume reviews at a round-table at work. The senior engineer I was working with at the time didn't do anything except POST requests to create users/sites/etc. to our 3rd party auth provider. He was, nominally, our senior web engineer, but when I asked him about our web app's architecture once he said "that's not really my job." This was the same person in charge of reviewing resumes.

None of this will come out during an interview and it's virtually impossible to suss out that kind of information from a few informal calls.

I don't want to be too hard on the manager(s) here. They probably don't want to be doing this in the first place and the engineers almost certainly don't want to be doing it. What's more though, they have no idea if you're a grifter! It's incredibly easy to give the right answers to questions or have the perfect tech stack experience and then be a royal jackass. Or, to just not do anything and get fired a few months later.

The exact same arguments around you know knowing the employer *apply to you as a candidate*. You could be the engineer who ignores messages for days at a time, who's mentally checked out and just doing this for a paycheck, or who's trying to company hop to earn a few raises in short succession.

This is the reason people hire their friends and people they've worked with before: They know what to expect. Be it good or bad, the information gap is bridged and, in a lot of ways, that's better than whatever the hell the interview process is supposed to tell you. 

## It's all a Fugazi

With all that in mind, know that the entire process is completely fake. 

Both participants are playing this weird game with one another where they are each attempting to not (?) tip their hands one direction or another and both people are trying to decide if the other person is lying to them (though nobody would admit to calling it that).

Most of the ways they are attempting to "verify" your credentials are also completely fake. I do not feel like my ability to design a small, command line app in X language is in any way indicitive of my coding abilities. Likewise, I don't really feel like being plopped in front of 3 other people and being told to design a solution to a problem I realistically know nothing about is going to tell you much about me.

Not only do I feel like these situations don't tell you much about the applicants coding ability, they also don't tell you much about their ability to communicate. Would you feel comfortable speaking in front of a virtual panel that you just met moments before? I really doubt it.

The irony here is, *the people who are interviewing you probably know this too since they got hired through the same process*. Which begs the question, why are any of us participating in this? Is it some weird loyalty test to the company?

My guess is, and I'm armchair psychologizing a lot here, is that the interviewers are suffering from a deep [survivorship bias](https://en.wikipedia.org/wiki/Survivorship_bias) coupled with a power imbalance. They survived the experience and they hold most of the cards here, which makes judging somebody else a lot easier.

Finally, it's a cruel reality of corporate employment that you essentially get no record of your achievements between companies. What I do at Optum has no way to be communicated to what I do at any other company. There's what I *say* I did at those companies, but that's again subject to the interview bias of "Is this person just telling me what I want to hear?" 

At least in university we had a GPA. However bad a proxy that was, it at least existed.

## Language Matters

I personally don't really believe that programming language(s) matter all that much. Pick the right tool for the job and use it. 98% of web apps will be fine even if you pick the *worst possible* language and I think developer skill/speed is much more dependent on their work ethic than the language.

That said, I obviously have preferences.

And hiring managers do too. In fact, in the morass of hiring that we've discussed above, the candidate knowing the language you are hiring for is a *huge* plus. Again, when you hire you're essentially picking a random person who you probably kinda like but that's about it. 

When choosing between two random people, you're never going to give the benefit of the doubt that X person is capable of picking up a new programming language. Especially when so many developers are *so* language preferential. No matter how much you say you can or are willing to pick up a new language, I heavily doubt you'll be given the benefit of the doubt.

I mean, you really mean nothing to these people and they know nothing about you. Why would they trust you?

## Final thoughts

In the end, hiring managers/engineers are going to hire people they like. And that's usually people they know.

There's nothing wrong with this really, but we should be up front about it.

My ideal interview would be to have three interviews. One 30 minute intro/touch-base to meet and all and then two 1-2 hour meetings. In the first, the manager should deeply discuss the company's product, in the second, the manager/engineer should deeply discuss something *you've* worked on. Avoid group work if possible.

And then make a call one way or the other.