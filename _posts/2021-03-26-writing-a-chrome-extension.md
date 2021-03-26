---
layout: post
title: Reflections on Building a Chrome Extension
slug: writing-a-chrome-extension
tags: [programming, posts]
author: Florian
---

If you want to learn how to build a web app, consider writing a Chrome Extension first.

### Context

I recently built the ["Three Gratitudes" Chrome extension](https://chrome.google.com/webstore/detail/three-gratitudes/pfjadpjmhanlgkpboobbfiecohncegfd). It's a pretty simple extension that locks your browser for 1 minute everyday until you write down three things you're grateful for. I was a bit of a Lenten project and also something I'd been wanting for myself.

Anyway, I was absolutely *floored* by how enjoyable it is to build a Chrome Extension and I knew I had to write about it.

### Chrome Extensions are mini web apps

Chrome Extensions basically have all of the components of a modern web app, but stripped down to their simplest implementation. If you're trying to learn the basics of building a web application, Chrome extensions provide everything you need:

1. A simple web "routing" system. Perhaps this is too simple to even call out, but in a Chrome extension, you just drop the html you want, navigate there in the URL bar and the webpage shows up. For new developers trying to understand the basics of HTML/CSS, you don't have to learn NodeJs, routes, [templating engines](https://floverfelt.org/posts/gist-secrets-reflections) or anything. Drop the file in and Chrome will render it at that path. Super simple.
2. A minimal but functional backend. Chrome provides a [messaging API](https://developer.chrome.com/docs/extensions/mv3/messaging/) by which the frontend of an extension can interact with the backend Chrome APIs. The interface mimics a basic REST API and it's a super simple way to introduce new developers to the concept of backend/middleware functionality (and how to communicate with it) without having to spin up a seperate app, write the endpoints yourself, or learn response codes.
3. A mini database. The Chrome [storage API](https://developer.chrome.com/docs/extensions/reference/storage/) allows you to store small amounts of user data in Chrome's local storage or cloud sync storage. For very basic CRUD apps, this is probably all you'll need. It's doesn't use SQL or anything, but it introduces the concept of persistant storage and how/when to use it. If you want, you could even drop a SQLite database into the extension and use that.

There's a few other minor things that are nice about Chrome extension development:

- You don't have to worry about cross browser compatibility. You can use ES6 JS or whatever webkit stuff you want and know it'll render the same across all browsers... Because you know it'll only render in Chrome.
- It introduces you to basic JavaScript. The Chrome docs pretty clearly do **not** use await/async, promises, or any of the latest JavaScript features. I think this makes it a pretty great place to learn. You have to walk before you can run, and you have to understand callbacks before you can understand promises (imo).
- It requires that you understand a 3rd party library. Basically every form of software development requires you to integrate with another codebase, framework, or library. Chrome provides [a very lightweight, well documented API to interact with](https://developer.chrome.com/docs/extensions/reference/). It's a good intro to development and integration of 3rd party tools.

The only real drawback I noticed to extension development was the lack of hot reloading. While developing, I had to manually refresh the Chrome extension in order to update the background (backend) scripts. The HTML/CSS/JS on the frontend hot-reloaded fine, but the backend did not and this got kind of tedious after a bit.

I would definitely recommend writing a Chrome (or any browser) extension. It's a lot of fun and has been one of my more successful side projects.

