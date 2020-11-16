---
layout: post
title: "Writing gistsecrets.io"
slug: gist-secrets-reflections
tags: [coding, node, tech]
author: Florian
---

This post is just a short reflection post on coding [gistsecrets.io](https://gistsecrets.io/home).

## Initial Thoughts

I'm pretty proud of this project. It:

1. It solves/reveals a real problem.
2. It uses a new tech stack I wanted to learn.
3. Is actually something I've been checking day to day.

So, all-in-all, a successful side project.

## Thoughts on Node, Express

[Node](https://nodejs.dev/) is really as easy as people make it out to be.
It takes just a few minutes to run the server locally and plugging in packages with npm is pretty seamless.

The same can be said for [Express](https://expressjs.com/). They really "just work" which is super nice.

Overall, I'd give the Node-Express tech stack an 8 or 9 out of 10. I'll almost certainly use it for other side projects in the future.

## Templating Engines

How did my entire collegiate education seemingly leave out [templating engines](https://expressjs.com/en/guide/using-template-engines.html)?
Maybe I just forgot? This was far and away the biggest confusion I had starting out building a web app and I'm sure others will too. 

Basically, you start off building and the first question you want to know is: How do I make something appear on the page? 

That's easy -- HTML. Everyone knows that. Ok, now how do you get the server.js file talk to the HTML.

The jump from the first question to the second is like getting hit over the head with a mallet. This is about how my thought process went for the second question:

* Well, you use any one of these weird-other-language things called templating engines which are kinda-HTML and kinda-not.
* They all have cutsey names like [pug](https://pugjs.org/api/getting-started.html) and [handlebars](https://handlebarsjs.com/) which somehow makes them more confusing to me?
* pug is also [jade](https://github.com/pugjs/pug/issues/2184)?
* Don't use EJS because people say it's bad.

This is not really unique to Node. I tried searching for templating engines in Spring MVC and got pretty much the same responses.

My guess is that in the microservice world where we send a bunch of JS to the end user to perform AJAX calls to an API, templating engines aren't as necessary and stuff 
like [React](https://reactjs.org/) become more important.
I could be wrong though as I don't work on a project that uses React or newer JS stacks. I would like to do a project which incorporates Angular/React/MongoDB,etc. at some point though.

## const, lets, vars

The usage of these across StackOverflow, tutorials, etc. is incredibly confusing to new developers. I'm not a new developer but even so, nobody seems to use them or use them appropriately. Maybe it's because they're newer types and developers want to be backwards compatible? I'm not sure, but it makes jumping into JS confusing.

I primarily code in Java at work and say what you will about it, but it does not have this problem. If you define variables as public when they can be private, even the most basic IDE complains. Likewise, it just breaks if you define it as private when it needs to be public. I get that [duck typing](https://en.wikipedia.org/wiki/Duck_typing) makes things simpler for developers but I do wish the variable types in Javascript had more consistency among developers. It seems like nobody has a problem with mis-using consts as vars and lets as vars, which makes me wonder why they were introduced in the first place.

## What's Old is New

I tried to write the first pass of the app in simple JS. As a result, I wound up with like twenty chained callbacks and code indented halfway through the page.

I figured there had to be something wrong here, so I spent some time understanding the history of JS and [async-await](https://www.youtube.com/watch?v=V_Kr9OSfDeU). I re-wrote the code to match that pattern instead and it's a lot cleaner. Plus I feel like I rounded out my JS understanding a lot. That said though...

It's funny to me that the "cutting edge" tech stack took until 2017 to release a pretty basic try-catch syntax. I feel like this has been around forever in Java and elsewhere. I chuckled a bit when I learned that it's considered "advanced" Javascript.

## Npm is a Little Overrated

[npm](https://www.npmjs.com/) to me felt like a slightly better version of what I use at work - [Maven](https://maven.apache.org/). 

Instead of the clumsy and verbose pom.xml it had a settings.json file. Instead of [mvnrepository](https://mvnrepository.com/) there's just npm.

Maybe there's [nothing new under the sun](https://en.wikipedia.org/wiki/Under_the_Sun) but I found the differences between the two surprisingly minimal.

## Final Thoughts

I really like using node.js and thought this was a fun project. I'll probably continue using it because:

* I'm the only developer so my preference is king.
* It's dead simple to get up and running, especially now that I have a familiarity with it.

\- Florian