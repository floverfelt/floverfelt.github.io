---
layout: post
title: Things I Wish I Knew About Software Engineering in College
slug: things-i-wish-i-knew-about-swe
tags: [posts]
author: Florian
---

I've been at my current job for ~4 years now and I've been reflecting on that time a lot these days. More specifically, I've been thinking a lot about how my college experience with Computer Science/Software Engineering translated into a professional Software Engineering career.

## Things I Wish I Knew

(In hindsight, I was taught a lot of this stuff, but just never really internalized it.)

### Software Engineering Is Data Transformation

This took me a while to realize, but Software Engineering is really just data transformation. 

Frontend engineering visualizes data. Middleware engineering fetches and prepares the data for visualization. Backend engineering stores and normalizes data.

That was not as clear to me when I began building software, but the more I work on complex software products, the more it boils down to one of those three principles.

### You Rarely Build Things From Scratch

We discussed this a *lot* in the 2000 level classes at UVa, which is why I still remember it. 60% of spending, time, etc. of any software product is spent on maintenance. This is a fairly misleading statistic to begin with -- if Facebook rolls out a new feature they aren't creating a new product just enhancing an existing one. Is that maintenance? 

Anyway, every piece of software you build in college is brand new. This is actually a huge rarity in the corporate world. In my four years at Optum, I don't think this has ever happened to my team. We've always been working on existing products. That's not to say there's no opportunity to create wholly new things, they're just usually built on top of an existing tech stack or application.

In CS1000 (or 1001? I can't remember), we were given a "broken" arcade game built in [Swing](https://en.wikipedia.org/wiki/Swing_(Java)) that we had to fix as our final assingment. It was a pretty fun project - we had to reimplement the broken game loop, add back collision physics, etc. All the core code was there, it was just broken.

I didn't think too much of it at the time, but it was actually a really clever assignment. You got hands-on experience with what actual software development was like - being given a mess of a system and having to figure it out.

### Your Job Is a Group Project

My later CS classes (~2000+) all were designed around this premise and that was another great idea that I didn't quite grep the meaning of at the time.

People don't magically change when they get a job. Money only motivates so much. 

That guy who showed up to group projects and never said anything? He's now you're coworker. The dude that tried to rewrite the entire project the night before it was due for no apparent reason? You're inheriting his legacy codebase! The TA who never responded to emails about a project and didn't help during office hours? They're your PM!

You get to work with a lot of talented people as well, it's not all bad, but the point is -- people are people. They don't really change and what you're experiencing in college is probably a pretty good analogy to the working world. 

### Learn The Assumed Knowledge

There's a ton of things I learned *very* quickly when I joined Optum that were either glossed over in college or we're so ridiculed by my peers that I thought it was completely silly to learn at the time. 

For example: People complained ad nauseum about having to learn Agile methodology in a class because "your employer will teach you that anyway." This was not true. Having to explicitly learn it made my transition to the working world a lot easier as I could get into the daily rhythms and habits of the team a lot quicker. I also understood the context of the ceremonies a lot better which made me appreciate why we were doing them. 

On the other hand, a lot of professors, TAs, etc. assumed we would naturally understand Git. I did not nor did my peers. This is partly because you don't really need it in small, transient group projects. It's only really valuable with large software products built across longer timespans. I did not get this and most of the adults-in-the-room assumed we got it.

Likewise, learning the *nix commands was completely skipped. We'd basically just copy commands in and pray they worked without understanding what we were doing. Even basic stuff like cd and ls felt like magic in college. Maybe this was just my own shortcoming, but I wish I had spent more time understanding command line functionality given how ubiquitious it is in modern software development.

Computer networking was also surprisingly useful and surprisingly downplayed during college. I took the optional "Computer Networks" (3000 something) elective for this very reason, but stuff like reserved address spaces, ports, and response codes are vital to pretty much everything you do, and yet no professor really taught it. It was more just assumed that you knew 127.0.0.1 is localhost which means your computer which means your computer is running a webserver.

Finally, and most egregiously, the database design class was horribly ridiculed by everybody. This could be because the professor was... not great, but I also frequently heard the argument that "you can just learn SQL online". It is true that you can learn the SQL *syntax* online, but databases are a totally different beast that are incredibly fascinating. They're also quite literally the backbone of any application. My first day at my job we wrote SQL pipelines to migrate data into the reporting databases. It was instantly helpful and a real shame that more people didn't appreciate it at the time.

## Final Thoughts

Overall, I think UVa did an excellent job preparing me for a Software Engineering career and I'm grateful for having gone there and for the things I've learned since.

