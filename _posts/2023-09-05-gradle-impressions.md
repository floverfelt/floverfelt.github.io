---
published: true
layout: post
slug: gradle-impressions
tags:
  - posts
  - coding
author: Florian
---

[Gradle](https://gradle.org/) is a build tool for people who like build tools. And I really like build tools.

Much like [Kotlin](https://floverfelt.org/posts/kotlin-still-not-impressed), I used Gradle briefly at my last job and have lately been toying around with it on one of my side-projects. I really hated it at Optum, but looking back that was much more likely the [circumstances](https://floverfelt.org/posts/corporate-america-a-new-product) and much less likely the tool.

All told, I really enjoy Gradle and will likely be reaching for it for my next projects. That said, I think the judgement really comes down to your mileage with the following.

## The DAG

The biggest challenge migrating from Maven to Gradle is the DAG - the directed acyclic graph - model it uses. Maven executes in a [linear build cycle](https://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html).

Gradle doesn't. It breaks your build down into distinct tasks, arranges them into a graph, and executes them in parallel. *This is incredibly confusing at first!* And likely where most people jump ship from the whole thing. Gradle - the tool - does a solidly *OK* job of trying to make this transition simple, but I hate the way your expected to upload a [build scan](https://scans.gradle.com/) to do this. 

Maven trades off simplicity and convention for power and speed (pretty much) wherever it can, and that's a fine tradeoff to make, but Gradle takes the opposite side of that trade every time. If Gradle can be more complicated but more powerful, it'll do it. If it can be faster at the expense of ease, it will.

It's a mindset shift, but once you're freed from the (semi-arbitrary) phases of the Maven build, you'll really see the power of this - parallel execution, build caching, environment setup - you can really do basically anything, quite speedily.

## Groovy/Custom code

How much custom code are you trying to execute during your build? If it's a lot, then Gradle is a godsend. 

I've written several Maven plugins, and they're great to write, but they require a lot of overhead to do [relatively basic things](https://github.com/floverfelt/find-and-replace-maven-plugin) in Java.

Gradle let's you run any code, wherever and however you want during the build. At work, we double a lot of our Maven "builds" as local environment configurations - executing S3 commands, setting up services, that kind of thing. 

Maven is... not great for this. I don't want to recompile my code just to do something totally unrelated like creating a local sample database. With Gradle, you can not only skip the tasks you don't need, you can write the code directly in the build file instead of using something like [GMavenPlus](https://github.com/groovy/GMavenPlus). 

Unfortunately, even with Groovy/Kotlin, the JVM is just not great at system/scripting style coding. The File/Path/InputStream/FileInputStream type objects are so convoluted and clunky that even basic file manipulation requires a multitude of null checks and object wrappers. I'm not really sure there's a way around that given that it's a *Java* build tool, but still.

## What do you want your tool to do?

Of course, all of that is *totally pointless* if your build is just... building Java code.

I think a lot of people misunderstand Gradle. It doesn't really shine as a tool for assembling a simple jar - Maven is far better for that. It shines as more of a build platform - for doing a lot of complicated tasks quickly in a JVM ecosystem.

There seems to be two camps among software engineers - those that think a build tool should just build the code - and those that say - well, I'm already building my code, let me do a few more things... If you're in the later camp, you'll love Gradle - so long as you can get over the learning curve.

