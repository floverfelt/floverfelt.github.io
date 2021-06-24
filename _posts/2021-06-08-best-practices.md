---
layout: post
title: Are software engineering "best practices" just developer preferences?
slug: software-best-practices
tags: [posts, software, programming]
author: Florian
---

My housemate the other day asked me something to the effect of "How can Software Engineers call themselves engineers when there's no rules, governing bodies, or anything to stipulate what true Software Engineering is?"

The parallel he drew was to another friend who's a Civil Engineer. His friend had to be state certified and build everything to certain codes that stand up to specific stressors and inspections.

I gave him the usual answer about how Software Engineers deal with low stakes and high iterability compared to Civil Engineers, but, honestly, he has a point. 

Software Engineering is *really* frustrating because there's basically never a "right" answer and so most decisions come down to "whatever the senior engineer wants." This is probably why people feel [imposter syndrome](https://en.wikipedia.org/wiki/Impostor_syndrome) so much in coding: You can't do it "correctly" if "correct" is "whatever the guy who's been here longer wants."

Don't believe me?

## Some Examples

Java is infamous for its verbosity. I was working on a Spring Boot REST API a few months ago and the senior engineer had defined every single service class as an interface and then implemented that interface in an actual @Service. The interfaces weren't extended by multiple classes, this wasn't an external library or a dependant, and there were no plans to implement additional classes later. The logic from the senior engineer was that the interface represented the "contract" and the class the business logic.

I thought this was silly. Just have a single class which handles both - it's easier to read, it's a smaller code base, and we have unit test coverage if somebody tries to alter the "contract" of the class anyway. Plus, we can always add an interface later.

Who's right here? Who knows! The app works either way, and it's still maintainable just a little more annoying (imo).

Or how about [version control](https://news.ycombinator.com/item?id=26582912)? Probably the single most ubiquitous aspect of Software Engineering. Should you squash commits? Should you rebase them? Is that lying? Should commits be a record or documentation? There's not a good or even right answer here.

How about [testing](https://news.ycombinator.com/item?id=18039103)? Good? No?

As I type this, I'm in a discussion about whether it's better to pass a few unnecessary parameters to simplify a bash script's internal logic or pass fewer parameters and make the bash script more complex.

## Some Thoughts

I guess this is the fun of Software Engineering - there's a million tools to choose from and you can choose whichever you prefer, but I also find this tiring at times. You never feel like you've mastered the profession because some guy can bloviate about how what you did was inferior to *some other thing he prefers for some pedantic reason*.

At the end of the day, you wind up in a lot of fairly pointless arguments about tech stack and coding conventions that 99.9% of the time don't make a bit of difference to the final product.