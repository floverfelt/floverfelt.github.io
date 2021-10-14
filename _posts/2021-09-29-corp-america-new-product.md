---
layout: post
title: The World of Corporate America, A New Product
slug: corporate-america-a-new-product
tags: [posts, work, life]
author: Florian
---

I was recently roped in to develop a new product that Optum is offering. It's basically a tool to map data fields to certain other data fields based on user input. Not super exciting, really, basically just a dynamic CRUD app. The app was said to have "high visibility" to Vinny, our CTO, and was being built out to serve only internal users initially. 

It did *not* need to be hosted anywhere, it did *not* need any user authentication, and it did *not* need basically anything beyond raw functionality.

In short, this is something you could conceivably build in a long weekend. We just hit month three.

## The Pitch

The pitch of this product (for me) was that we'd be using a cutting edge tech stack to build a green field product and I'd get to work on the front-end - something I've been wanting to get more knowledgeable about for a while. Best of all, I'd get to do this on a "high priority" product with another senior FE engineer who could show me the ropes.

This has not panned out.

## Initial Things That Happened

I joined the team a week after they had chosen the tech stack, and that was pretty much all that had been done. There's only three engineers on the team - myself, the FE guy, and a backend developer.

I hopped on a call with the front-end guy who pretty baldly states that he "has no clue what this app does" or "what he's supposed to be doing."

I bring up the fact that we'd essentially chosen a tech-stack having no clue what the application does, and I get chastised by the manager because "we've already done that work you just weren't here." FE does not chime in this conversation, in fact, he skipped the stand-up where we were discussing this.

I then had to setup a meeting with the PM to find out what the app is actually supposed to *do* so that we could choose a framework and also so that we would *actually know what the app was supposed to do*, which seems important. This is all to the chagrin of our manager who is very stressed that we won't be able to deliver an alpha/POC version of the application *by mid-December*.

Out of that meeting, it turns out that there's also a UX guy on the team who built a bunch of wireframes for the app. It's also made known to us that there's an official "UI Toolkit" we need to use - basically a collection of React and Angular components we're supposed to stitch together.

None of the components in the toolkit look like the wireframes and the senior FE doesn't know anything about the toolkit, despite it being an "Optum standard." We are then told by a random senior manager that "it's a requirement to use the toolkit and for everything to look like the toolkit." Which is totally different than what the wireframes look like...

So, then, we have to have another meeting with the Toolkit team to understand their role in our product. They are incredibly pleasant people who basically say "Use as much of this library as you can, but don't worry about adding third party components if you need to." The UX guy then (randomly) joins our standup for the first time and pretty much says "Yeah, I don't really care if the app doesn't look like the wireframe I built" and the PM agrees. Which begs the question, *why do we have a UX engineer if we're just going to ignore what he builds?* 

In the meantime, the backend dev has chosen Kotlin to build our Lambda functions in. For no real reason other than he likes it.

Oh well, at least we can start building now right?

## Planning, planning, planning

We use a JIRA-like tool to track all of our software development in. The PM and manager had gone through and logged all of the work we needed to do for alpha. Great work! They had not put any points, description, or acceptance criteria on the tickets.

One would think we would go through these stories and add descriptions, estimates, and any other stuff relevant to the work we needed done.

We did not do this.

Instead, we had multiple, *hour plus long meetings* where we discussed, multiple times, how to handle race conditions in our application when two users saved at the same time. This is an obviously essential question to be asked at this stage of development.

We then proceeded to T-shirt size all the stories. But, instead of putting them into our product management tool, the manager wrote them all in Notepad and then never shared them with the PM, so we wound up doing this exercise twice one day when the manager was on PTO. 

This took about two weeks because "We need to get the estimates right to deliver the alpha by mid December." Ironically, with the amount of time we spent planning, a solo-dev probably could have just built the app.

## Development

At this point, we have one developer working on the backend and one developer on the frontend (me). The "senior frontend engineer with 10 years of experience building applications" has stopped joining any standups, responding to messages, or doing much of anything.

The backend isn't built, so I went ahead and built all of the static assets the site needs - the header, footer, and static landing pages. We populated the entire thing with [Lorem Ipsum content](https://en.wikipedia.org/wiki/Lorem_ipsum).

Optum does a weird thing where all their headers are images and the product name is also an image, which you have to request from the branding team. I submitted this request - the branding team forwarded that request to the "Naming Committee", who forwarded that to the PM, who then sent a survey to (??) asking for input, and then everybody forgot about it and moved on.

At this time, a Chinese QA engineer, who randomly joins our standups from time-to-time, messages me and asks me to translate our application into English instead of whatever language it's in.

Nobody seems pleased that we've at least started to build this app. The manager complains that we are too busy "putting the paint on the car instead of building the engine," despite *literally having a full time backend engineer building this app right now.* He then frequently requests that we "give updates on the app's progress" even though he would ask for these updates moments after we just gave him an update in standup.

In order to avoid this confusion, I decide to setup a demo site so that we're all on the same page. This was *not* budgeted for, but I figured it would save us all a lot of pain if we had a single source of truth instead of just talking about what the app.

I then get told off multiple times for creating an S3 bucket with the wrong permissions while trying to set this up. Never mind the fact that Optum's AWS policy allows you to *create* buckets in AWS but prevents you from deleting them or modifying them. So, you're stuck with any mistakes you make while POC'ing something.

At this point, development starts going semi-well. We build the first pass of the API endpoints and most of the initial core functionality. This takes ~2 weeks.

The senior frontend engineer continues to not respond to messages. In a galling act, the manager asks us all to rank how much work he's doing in hours *in front of the entire team*. I thought this was totally inappropriate to do since it's a bit of a public humiliation for the guy, but I say he's *maybe* doing 1 hour of work a week.

In 1-on-1's I follow up and pretty much say that if this guy doesn't want to be on our team, we don't need him. Just let him stay on his old team.

Instead, the manager, who's been absurdly strict about not adding any new work to our timeline, decides to create a unit testing story for the guy to do. Thank god we are *frontend unit testing* a POC/alpha application. I get tasked with following up with this guy to "kickoff" the story.

He *finally* responds and says "Yeah, this is just busy work. I've never seen unit tests be valuable to the front-end, but managers love them." So, we all had just tacitly agreed that we had invented busy work for this guy to do to justify paying him for twenty hours of work.

In the meantime, the guy who commissed this entire project retired.

## The Demo

There is now a fabled demo to take place to the "stakeholders." 

I suggest we just send out the demo site to the stakeholders before the meeting to get feedback and also give people time to use it a bit so we avoid all the stupid one-off questions like "why is this button green?" and can get into the meat of the app. There's nothing there really except a POC and any data they put in we can just nuke with one of our Lambdas and reset it all.

This suggestion is met with an incredibly cold reception. The PM says that our app's use case is so confusing that nobody will understand it without our context anyway. One would think *this in and of itself is good feedback that maybe we should explain the app in the app.* But whatever.

Meanwhile, the manager and the other devloper are very upset that I built an "Add" form and that it's exposed in the app because "we don't want to demo any functionality that we haven't agreed to deliver." Despite *none* of the buttons working in the app, I have to hide the one button that we actually implemented because that's bad that we implmented it.

The demo goes fine in the end, nobody asks about any of the buttons.

## The Build

At this point, it becomes imperative that we have a CI build which runs on each PR - it needs to build the app and run any tests we have. I picked this up. 

Since we're building a server-less Kotlin app (a bizarre decision in and of itself), we're using Gradle as the build process. When we began this project, the senior manager asked the other dev to convert the build to use Maven since that's what all our other build processes use. He just ignored this and never did it.

The other dev also wrote all of our unit tests as integration tests - requiring a live database connection. I then spent a week trying to get Docker-in-Docker working on Jenkins for the mongoDB we use. I mentioned that Gradle is a little slow to build because it spins up a daemon processs first. 

The manager loses it over this. Stating that having "30 minute build times is unnacceptable for developer productivity."

At no point did Gradle *ever* take 30 minutes, nor did it *ever* take more than a few seconds to build locally. It was just when it was running on Jenkins that *the entire build* took 10 minutes - including the frontend and Sonar scanning.

But I nevertheless spend 2 days back-porting the build to Maven because build times will really slow down a project! This is all happening while one of our developers has not done *anything*. What tends to slow down projects, is the project never being built.

## In the end...

I want to grab everybody involved in this project and shake them and yell "this app does not exist!" It doesn't matter if we have unit test coverage on an application that nobody is using and is *scheduled to change*.

It doesn't matter if the build times are slow on a CI pipeline for an application that only two developers are building! 

It doesn't matter if people see a button that includes functionality that we haven't promised! None of this is real! 

We need to build the app, and get it in front of people. We need to decide what it's going to do, and what we're going to optimize for.

What we don't need are all these corporate ["best practices"](https://floverfelt.org/posts/software-best-practices) that are doing nothing but hindering us and wrapping us in pointless arguments about libraries, testing, and other minutiae.
