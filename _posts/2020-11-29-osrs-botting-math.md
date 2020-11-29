---
layout: post
title: The Math of OSRS Botting
slug: osrs-botting-math
tags: [math, osrs, video games]
author: Florian
---

## OSRS Botting Math

I've been thinking a bit about [botting in OSRS](https://oldschool.runescape.wiki/w/Botting) and was curious about the claims 
that the [bot owners are making 200k a year](https://www.youtube.com/watch?v=QaQbYODIukI&t=102s).

Calculating the costs/profits of a bot is pretty straightforward and a fun way to use some of that algebra that everybody complains about never using.

## The Equation

First, some stats to keep in mind:

- 1 million (1m) gold (gp) in OSRS is worth ~0.5 US dollars today.
- 14 days (336 hours) of membership is worth [~6m gp](https://secure.runescape.com/m=itemdb_oldschool/Old+school+bond/viewitem?obj=13190).

These assumptions are roughly accurate (at time of writing) and make the math easy.

So, we can throw together the following equation to estimate the gp a bot will make:

`y = z(x) - 6(floor(x / 336) + 1)`

`y` = the amount the bot makes (gp)
`z` = the rate of money making (in millions of gp per hour)
`x` = the time worked (hrs)

We'll assume the price of the bond is static at 6 million gp for now, though that could be pulled out to a seperate variable.

The first half of the equation is a simple rate multiplied by time - `z(x)`. But, each bot also has a cost of 6 million gp at least and will cost 6 million gp
for every additional 336 hours it's active. If it's a free-to-play bot, we can lop off all of that.

To get the profit of the bot in dollars, simply halve y since 1 million gp is worth 50 cents. Likewise, you can multiply the result by the number of total bots
to assume you're running a "bot farm."

There's lots of other factors at play, like the flutuating cost of bonds and the flutuating costs of the gp, but let's leave as-is for now.

## Maximum Rates

Going off the [wiki](https://oldschool.runescape.wiki/w/Money_making_guide), a top tier bot can make ~3 million gp/hr. I skipped through some of the top listed
rates because those things aren't super bot-able to begin with and I think the wiki grossly over-estimates the rates anyway.

In a day, your bot would make:

`y=3(24) - 6(floor(24/336) + 1)`
`y=72 - 6(0 + 1)`
`66m`

So, a high level bot would make you roughly 33 dollars a day or 1.375/hr.

A person making $200,000 a year needs to earn about $550 a day (200000/365). So, you'd need at least 17 bots doing this (ceil(550/33)) 
to earn that kind of money.

This is where my assumptions start to break a bit. Your account wouldn't just spawn in making that amount of money, you'd need to sink time into the 
account to get it to that point, or, buy the account. An account even close to the 3m/hr marker is probably going to cost you 80 - 100 dollars (data on this is tough to find).

So, our new equation for a bot's single day total is:

`y= 3(24) - 6 - 100(2)`
`y= -122`

Yeah, you're in the hole a bit, let's bump up the time frame a bit to 335.9 hours (max without requiring a new bond):

`y= 3(335.9) - 6 - 100(2)`
`y= 801.7`

So, in 14 days, you've made 400.5 dollars (28.5 dollars/day, 1.19 dollars/hr). This would require a bot farm of at least 20 bots to hit the 200 grand a year figure.

Certainly not impossible, though again this is being extremely generous and assuming 0 bans on the bots and perfect efficiency.

## More likely rates

Let's take a more reasonable estimate and say most bots are probably making 300k/hr.
This is roughly the range where you don't need a ton of requirements so bots don't have such a high startup cost.

Again, assume no bans and perfect efficiency:

`y= .3(335.9) - 6`
`y= 94.77`

Each bot is then making 6.76 a day or 14 cents an hour. At that rate, you'll need 82 bots chugging away each day.

Probably though, these bot farms are just trash bots earning 100k an hour so:

`y= .1(335.9) - 6`
`y=27.6`

In its bond time, the bot is making 13.8 dollars or 98 cents a day. So, you'll need 562 bots to hit the 200 grand/year.

## Conclusion

Yeah, it's certainly possible to make this much and my math squares with what the guy in the video says.

Is it a good idea? Probably not.
