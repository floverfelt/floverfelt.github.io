---
layout: post
title: What happens when you hit the front-page of HackerNews
slug: hackernews
tags: [posts, work, life]
author: Florian
---

[This blog went semi-viral](https://news.ycombinator.com/item?id=28706393)! I submitted my post ["Are software engineering "best practices" just developer preferences?"](https://floverfelt.org/posts/software-best-practices) kind of on a lark to get some feedback on my writing, and, wow, it struck a nerve.

The post stuck around the front page for a day or two, and then floated down to page three (coincidentally) by day three. At day four, the discussion and traffic was essentially done.

In that time, this blog saw ~10,000 pageviews, and I got four emails from various people. Somebody else also shared the post on LinkedIn and tagged me in it. 

## The Spirit vs. The Specifics

My biggest takeaway from all this is that when you read a blog post (or any opinion media for that matter), you should look for the *spirit* of what somebody is getting at and not the *specifics*. Obvious caveats apply here but *generally* this is my read on things.

I wrote the original post to express my frustration with the vast amount of minutia Software Engineers seem to argue about and then posit that most of this is largely preferential rather than codified industry standards, norms, or even requirements. I think the spirit of the post came through and [that's reflected in the top comment](https://news.ycombinator.com/item?id=28707349) and [the general discussion people had](https://news.ycombinator.com/item?id=28707909).

The people who really missed what I was getting at tried to take everything literally. I did not write the post [to get (yet more) feedback on how to "correctly" code my specific examples](https://news.ycombinator.com/item?id=28706908). I also did not write this post to [get help in responding to my friend's question](https://news.ycombinator.com/item?id=28706793) which a few people responded to. The latter can be a little more forgiven because discussions of professional engineering orgs are at least germane to the conversation and I could very well not know about them depending on my background.

I also found it pretty hilarious that a lot of the discussion devolved into the [same](https://news.ycombinator.com/item?id=28710455) ["best practices"](https://news.ycombinator.com/item?id=28706862) [discussion](https://news.ycombinator.com/item?id=28708222) I was lamenting in the original article. This is exactly what I was frustrated about when I wrote the initial article.

There were plenty of people who got the spirit of the article and [simply disagreed](https://news.ycombinator.com/item?id=28710607) or [had a different take](https://news.ycombinator.com/item?id=28706979) and that was super valuable. I try not to write this blog for other people, but I should have been more clear about what I was referring to in "best practices" and also provided more rebuttal to even the most basic of principles like DRY, version control, and dependency management.

A small quirk of the Spring Boot example I gave is that I actually *didn't* implement the interface as the senior developer requested. The tone of the post certainly suggests the opposite, but in that example my preference won out in the end. This didn't seem relevant to the broader point so I omitted it. Again, I didn't want to get into *who was right* in those examples. I wanted to discuss the broader point about *why we constantly have these discussions in the first place*.

Which is why it was really funny that [some people suggested there was no way my code could even work](https://news.ycombinator.com/item?id=28712365). It did work! I tested it and also wrote the [unit tests for it myself](https://news.ycombinator.com/item?id=28706891). And it's running in prod now!

The point being here: Giving stories and examples hits a point of diminishing returns. There's *no way* I could have given the full context of the team dynamics, application architecture, and outcomes that would have satisfied people reading, and even then they likely would have said everything needs more context. Of course it does! You're reading a blog post of my experiences, not living them.

I read a great post [about work at a big company](https://rachelbythebay.com/w/2021/08/28/big/) and the [response in HackerNews was oddly mean](https://news.ycombinator.com/item?id=28344677) with people calling the author a [Karen](https://news.ycombinator.com/item?id=28345853) and an ["awful person to work with"](https://news.ycombinator.com/item?id=28345241). There is quite literally *no way* the author could convey everything that was happening day-by-day, the culture, and the context of the work environment in a blog post ([she wrote a similar response](https://rachelbythebay.com/w/2021/09/01/dash/) to the one I'm writing here).

It's more important to respond to the *spirit* of what the person is getting at and not get hung up on the *specifics* because the other person always knows more about their own experiences than you do, and you should probably trust that they are *generally* right. 

## Are "best practices" just preferences?

Yes, mostly. I don't think my opinion has changed all that much, but I took a few points to heart.

I was swayed a lot by the people who said I was conflating very basic principles like version control and DRY with toolsets and stylistic decisions. There is some truth to this, and perhaps I'm [too much of a fish in water](https://www.newyorker.com/books/page-turner/this-is-water) to appreciate them. I guess the problem is, we don't often call those things "best practices" since they're *so* basic. What gets called a "best practice" is everything on top of those principles which immediately fractures into a huge set of ideas, styles, etc.

What I've been thinking about more at work these days is language choice as evidence of preference. We have [literally](https://clojure.org/about/rationale) [four](https://groovy-lang.org/) [languages](https://kotlinlang.org/) [that](https://www.java.com/en/) compile to the *exact same thing*. For an industry where most developers are obsessed with simplicty and terseness, this is bonkers to me. I understand the arguments around certain languages being built for certain use cases, but by and large, most software can get away with boring old Java or any other language really.

Like some people pointed out in the comments, the issue is really around being unified as a team to a single preference, not the existence of all these preferences, and I agree with that. Ultimately, software is built and maintained by people and that should be the focus, not the tooling.
