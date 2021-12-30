---
layout: post
title: Thoughts on Angular
slug: thoughts-on-angular
tags: [posts, tech]
author: Florian
---

I've been working with Angular quite a bit recently and figured now was as good a time as any to jot down my thoughts on it.

So...

## How's Angular?

It's honestly not that bad. I've heard a lot of complaints about it and it's [the most dreaded web framework on StackOverflow](https://insights.stackoverflow.com/survey/2021#section-most-loved-dreaded-and-wanted-web-frameworks) but Angular is really pretty decent.

The first thing that you always hear about Ng is that it's a full-fledged framework. This means you can't just drop: `<script></script>` in and use it. You have to use their CLI, compiler, and build tools to create your web app and work within their framework.

I suspect this is why most people *hate* Angular. [As I've written about before](https://floverfelt.org/posts/software-best-practices), developers hate phony "best practices" or imposed structures on how they write code. We've developed entire languages, frameworks, and a multitude of other tooling to basically allow any developer to choose exactly how they want to code.

Developers (should) love this! It's an amazing time to build web applications. You can use plain HTML + JavaScript if you're a purist, you can use PHP if you want everything in a single file, you can use NextJs if you want the entire tech stack in cutting edge JavaScript... I could go in. The trend right now is to complain about this multifurcation of the world, but if you take a step back, it's actually a pretty amazing time to be a web developer.

Unfortunately, the multiplicity of techs is a horrible bane on companies. You have to hire a "React" dev now, not just a generic web dev. If you do hire a React dev, they need to also know [Redux](https://redux.js.org/) and [a slew of dependent libraries](https://reactrouter.com/) that go along with it.

Angular, for all its faults, gets rid of this problem. If you know or use Angular, you know it's [routing](https://angular.io/guide/routing-overview) system, it's [state management system](https://angular.io/guide/architecture-services), and it comes with [testing built in](https://angular.io/guide/testing). These are all *incredibly important things* to have in a web application. The odds that you'll have to add this stuff anyway is near certain, so I don't really have a problem being forced into the Angular structure/world if it means you get all this stuff "for free."

Finally, the imposed component structure is a nice benefit when you're (read: a company) churning developers regularly. You don't have to hunt through the code to find out that one developer stuffed all the CSS into a single file, while another did solely inline CSS, and a third component scoped it at all the way the React docs recommend.

## How's working with Angular?

Angular is solidly *ok* from a developer perspective. It feels *a lot* like Java ported to the frontend. In particular I found their implementation of JavaScript-in-HTML a little confusing. The portions that could be JavaScript look way too much like traditional HTML tags to differentiate the distinction. My IDE was too much of a crutch for me here.

Otherwise, I enjoyed using Angular. I would say that it was actually a lot simpler to use than (*gasp*) React. It generates a *lot* more files than React, but the state management I found to be a lot easier to grep. There's no virtual-dom oddities, [useEffect](https://reactjs.org/docs/hooks-effect.html) strangeness, or state management quirkiness. I could simply set a stateful variable and then use that variable (such amazing! much wow!) instead of copying into the state and then waiting for the React state to trigger an update to that variable.

Importantly, Angular also allowed me to pretty much do whatever I wanted with the state. I could share it around components and delegate it however I pleased. It didn't force me to [think in React](https://reactjs.org/docs/thinking-in-react.html) or whatever nonsense and as a result multi-nested component trees became a lot easier to work with.

I also didn't have to think about the whole [hook vs. class thing](https://reactjs.org/docs/hooks-faq.html). The Angular CLI basically tells you how to structure your component when you use `ng generate` which I liked. There's some version-by-version differences when you try to look up how to do certain things, but by and large it was pretty consistent.

I still think [Svelte](https://svelte.dev/) is the best developer experience I've had by far, but I was pleasantly surprised by Angular. I think it's OOTB feature set makes it a pretty compelling choice for building large scale web apps.

## In Short

My few sentence summary: Angular is the Java of the frontend. Enterprises love it because it provides rich functionality, and structure in a fairly ambiguous dev world. Developers hate it because it's verbose, generates lots of files, and isn't X technology that they would use.

