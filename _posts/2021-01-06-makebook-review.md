---
layout: post
title: A Rambly Makebook.io Review
slug: makebook-review
tags: [books, review]
author: Florian
---

I've been locked out of my work computer for the last several hours with no end in sight, so 
now seems like as good a time as any to review [Pieter Levels](https://twitter.com/levelsio) [makebook](https://makebook.io/).

I bought it on sale for $15. The TL;DR: It's a decent-ish read with a lot of flaws - 6/10.

## Levels Philosophy

Levels essentially thinks that you should build, and build a lot. You shouldn't worry 
about tech stack. Solve problems that are relevant to you as you'll be best suited to solve
those problems. 

This probably captures 90% of what the book says. If you're a Software Developer or have some
coding experience, I wouldn't even bother buying it and just watch the [video](https://www.youtube.com/watch?v=6reLWfFNer0) he links instead.

## What He Gets Right

He's obviously right about building and building a lot. This isn't anything new - if you want to get better at something you have to practice it. If you want to get better 
at launching small businesses on the internet, build a lot small businesses on the 
internet. If you want to get better at coding, code more. Etc.

That's not really a novel point, but it's not wrong either.

The same goes for most of the other things he says in the book. Yeah, you should automate 
your company, be ethical, etc. 

I'm blowing by a lot of this because (1) I don't want to spoil the book, but (2) it's really obvious stuff that doesn't require a lot of comment. I'm coming at this book 
from the perspective of a Software Engineer who knows the importance of automation, CI, etc. 
as we talk about it every day at work.

If you're stumbling on this book as a sales person or somebody not embedded in the tech 
community as much, I'd bump the recommendation up to a 7. The problem with the book for me 
is how common sensical a lot of what he says is, but I could be biased by simply being 
surrounded by that for much of my day.

## Thoughts on "Being Original"

I see this crop up a lot and it's not unique to this book. The idea is if you want to 
do something great you have to be original, which in this book is defined by:

> Get ideas from your life experience. Get outside. Become original. 
> Do crazy stuff that you're scared of. Jump off cliffs (do it safely). Ask people you like out. 
> Walk into random office buildings. Jump fences. Crash hotel pools. Whatever makes you different. 
> Don't be so scared! Live.

This reminds me of something I read in [Feed](https://en.wikipedia.org/wiki/Feed_\(Anderson_novel\)) years ago.
Essentially, one of the main characters laments that even the things she considers 
to be special experiences are fed to her by companies and set by the culture.

I feel like that's what's happening here and something that's missed in 
a lot of cases. Weird people do *weird* things. And I mean truly weird. My friend's 
wife has spent the last four years studying a single ribosomal transport RNA (no 
idea how accurate this is). That's a *weird* thing to do. 

The people writing Open Source Software obsessively are *weird*. Most people don't want to do that and they don't. Most people are pretty down to go on dates and go skydiving.

The point is - the people that spend years working on esoteric and seemingly pointless projects are truly weird. Levels is describing what an Instagram influencer thinks is weird.

If you want to be truly weird, have intersecting interests, don't talk about them, and 
probably obsess over at least one of them. Jumping into a hotel pool will not help 
you here.

## The Implicit Hatred of Companies

I recently read ["Big Business: A Love Letter to an American Anti-Hero"](https://www.goodreads.com/book/show/39863479-big-business).

I wish more people would read that book these days. Yeah, companies do a lot of bad things 
but they're also just a collection of people. They reflect people's failings because 
they are just groups of people.

Makebook seems to be proposing that we should all create these one-off problem solving apps and make enough money to live independently or remotely (?) I guess and never attempt to 
solve problems which we don't understand. His response to this critique is laughably bad:

> I get it. And I see the criticism there, but then, it's hard for anyone to solve a problem outside the context of their own subculture, city, country, continent, region, income class and gender, because they're not experts on it.

Companies literally exist to solve this problem. I have no direct experience with insurance code billing, ER readmissions, etc. but my job at Optum allows me to improve those problems 
by joining with others who *do* understand it but don't know how to code a solution. 

We pool our talents and create something better than any indiviual alone.

I'm not lambasting the idea of making things to solve problems you have for yourself or 
running a side business, but I am against the idea that feels implicit in a lot of the 
indie hacker space: Working for a company = bad.

If everybody lived the way Makebook proposes that we live, we'd have a bunch of singleton apps that solve small-ish problems scattered across the world. Large scale systematic change and products would be basically nonexistant.

> If we can democratize access to computers and the internet (as we're doing now), people anywhere can focus on solving THEIR own problems and reap the financial (and other) rewards from doing that.

The real irony here is - he's relying on large companies to lay infrastructure, build the computers, etc. that indie hackers in small countries need to startup. Solo builders are generally not laying internet in sub saharan Africa.

## Tech Stack Doesn't Matter

He's right about this. In the long and short of things choosing between PHP, NodeJs, etc. is pretty irrelevant. Nobody outside of the tech world really cares how your website functions. That said though, I do feel like if you're a Software Developer, you should pick a more cutting edge tech stack, or at least a tech stack that you believe will be relevant to you. If you're going to build an app, you may as well pick up some new skills along the way? Most SWD should strive to be pretty language independent anyway, so it shouldn't be a huge ask to learn some new tech.

### Some Clarifications

I can't quite remember if it's mentioned in Makebook, but PHP is not dead and people don't hate it? It [literally powers 80% of the internet](https://w3techs.com/technologies/overview/programming_language). Weirdly, Levels has a massive bias for PHP which makes him get really defensive when anybody mentions Node or any other language. Yeah, you can build lean, but there's nothing wrong with the new frameworks that exist. React and Angular solve real problems for people building websites at scale or with disjointed frontend teams. Nobody is saying you *have* to learn them and they seem to be pretty well respected solutions to a legitamete problem. Like the tech stack comment above, you may as well learn it just don't obsess over it (which he does acknowledge).

> There's misconceptions about SQLite that it'd be slow or not scalable enough. That's bullshit. In many cases, SQLite is now faster than the filesystem (!) itself.

SQLite is also not misunderstood really. It works great for his use cases because (again) he's building one off apps that run on a single node web server. You don't need a distributed database for that and that's why SQLite works for what he's suggesting. That said, most people don't have this requirement. Most companies seperate frontend and backend teams and they also need to be able to load or update a database without touching the web frontend. None of this is "misunderstood" it's just guaging the cost/benefit of using one tech against another.

## Remote Work
