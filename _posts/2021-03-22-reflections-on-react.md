---
layout: post
title: Reflections on React
slug: reflections-on-react
tags: [programming, posts]
author: Florian
---

As a developer on a very old Tomcat/WAR application, I'm in a constant state of FOMO around the latest and (?) greatest developments in JavaScript. It's why I built [Gistsecrets](https://floverfelt.org/posts/gist-secrets-reflections) in Node, and why I wrote one of my latest, albeit failed, [endevours in React](https://github.com/floverfelt/floverfelt.github.io/issues/19).

I very much wanted to "get" React, and I can now say I get it. 

## Context

I used React and [NextJS](https://nextjs.org/) to build a basic CRUD style app called RateMyDay. This was a webapp in which you created a job to track and then the app would prompt you to rate how you felt about the job each day. You could then use RateMyDay to decide if you should quit your job or to chart trends of how you were feeling about your work throughout the day to better optimize your productivity and happines.

I built the create job form, the logging mechanism, user authentication, and a few other minor features before giving it up. I won't claim that I did everything *well* with React and NextJS but it was functioning and I feel like the experience gave me enough context to understand the frameworks and their purposes.

## Reflections

Let's start with what I liked about React.

First, the combination of the Javascript and HTML into a single file is truly exceptional. I recently wrote a [Chrome Extension](https://github.com/floverfelt/floverfelt.github.io/issues/23) in vanilla JS and HTML. My options were to either messily embed the JS into the HTML page  or source the JavaScript from another file and then toggle between the two files.

I went with the latter and it did get pretty cumbersome toggling between the two files to view the same page. React doesn't have this problem. Everything is lumped into a single JS file and you can move between the state (logic) and the HTML (JSX) seamlessly. This was really nice, and also not something I knew I liked until I didn't have it.

The actual reactivity of React was pretty cool too, though I didn't really take all that much advantage of it beyond form validation and a few other things.

React helps turn frontend development into more traditional software development. Components are (quite literally) classes and the state is another way to model class objects or fields. Those objects in turn respond to events and methods acting on them. People like object oriented programming, and React feels like object oriented programming .

As somebody who has written a lot of vanilla JavaScript, I can see both how and why people prefer working in React. It's simply a much more comfortable system for large scale products, especially if you're on a detached frontend team that *only* does JS/HTML/CSS work. 

All that said...

I don't think I'll use it again. 

For one thing, I think I fall on the HTML side of the JSX vs. HTML debate. It seems simpler to me and I'd rather work with the actual objects instead of an abstraction of them if I can.

I used React mostly in the context of NextJs, and I felt like both React and Next were evolving too quickly to be a good choice right now. I tried to primarily use component classes for my app because they made more sense to me and they're also the "original" React. I want to learn from the ground up and classes felt like the ground. But! [NextJs](https://nextjs.org/) frequently only supported hooks and function definitions. I couldn't mix and match them so I had to rewrite chunks of my app to basically just wrap the classes in functions so that I could use NextJs hooks.

If I had started out just using functions, I think it would have been easier, but I didn't and the documentation is a little poor because it's so new so I was stuck.

In the end, it all felt like... just a bit too much for what I was trying to accomplish?

Having to haggle with the state to inject contextual CSS, the cryptic errors, the constant copying of the state, etc. just didn't seem to result in all that much of a benefit. But again, I'm 100% *not* using this the way it was intended, so that's to be expected.

### NextJs

NextJs felt pretty much the same as React - a really neat product that I had pretty much zero use for. I liked the simplicity of it and the basically non-existant backend. It's pretty much taking the "[convention over configuration](https://en.wikipedia.org/wiki/Convention_over_configuration)" approach to the extreme. If you want an api, stick a JS file in the "api" folder. If you want a page, stick a JS file in the "pages" folder. You get the idea. NextJs has some great [documentation](https://nextjs.org/docs) that I loved reading and it's a cool system. I was able to integrate AWS Cognito relatively painlessly using their APIs & walkthroughs which I think is a good litmus test.

The only two things that bothered me about it are completely irrational and preferential. First, the blurring between the frontend and the backend *killed* me. I hated not knowing whether something was being server-side rendered or client-side rendered when it was on the same page. The docs helped a lot here, but it still bothered me.

Probably more alien to me is the modern trend towards serverless web-apps. From what I understand, [Vercel](https://vercel.com/), the makers of NextJs, split each page and api endpoint of your app into a serverless function. These serverless functions are all linked together into a web app and connected to whatever database you choose. 

This is a brilliant idea - you minimize cloud computing costs, it's highly scalable, and you don't really have to think about what your website is running on. I'm all for this! But, when I'm programming just as a hobby, I don't mind doing hosting stuff? It's fun messing around with EC2 boxes and breaking them in various ways. You can learn a lot about IP routing, subnets, firewalls, etc. by setting these services up on your own and something's lost when it's all done for you.

### Working my way through the JavaScript ecosystem

I really want to try [Svelte](https://svelte.dev/) next. It seems like a good hybrid between React and vanilla JS.

Going backwards a bit, I'd also like to build an app using PHP. It's definitely "stood the test of time" at this point and I want to see why.

