---
layout: post
title: Short positions do not have infinite risk
slug: short-positions-infinite-risk
tags: [posts, stocks, misc]
author: Florian
---

This is completely unrelated to most of the normal things I post about here. Stocks, shorts, options, etc. have been in the news a lot due to [GME](https://www.marketwatch.com/investing/stock/gme), [COIN](https://www.marketwatch.com/investing/stock/coin), and the money-mania we're experiencing and I wanted to post my thoughts on something you hear a lot from PFAs and the news about [shorts](https://en.wikipedia.org/wiki/Short_(finance)):

```
Shorts are a more risky investment because they have infinite risk.
```

For anyone unfamiliar, I'll summarize what this means in brief.

## Stocks vs. shorts

When you buy a stock, you own it. When the value of the stock goes up, you can sell it and make money on the sale. When it goes down, you can sell it but you will lose money on the sale. 

Trivial example: If you buy a $10 stock, and it goes up to $12, you earn $2 when you sell it. If the same stock falls to $8, you lose $2 when you sell it. 

This is simple and everybody understands it for the most part. What's critically important for this conversation is the **risk profile**. When you buy that $10 stock, you risk a fixed amount of $10. If the stock goes to zero, the most you lose is $10.

Shorting is the opposite of this. You are selling stock before you buy it. You do this by promising to buy the stock again at a later date. This allows you to essentially bet that a stock will fall in value -- allowing you to sell high and then buy low instead of the typical buy low and sell high.

Trivial example #2: If you short a stock at $10, and it goes up to $12, you lose $2 as you have to buy it at a higher price than you sold it for. If the same stock falls to $8, you earn $2 as you're buying it at a lower price than you sold it for.

Again, this conversation is about the **risk profile** of shorts. When you sell first, you have no idea where the stock price will end up that you'll have to buy at. There is no fixed risk of $10 like with a typical stock, because the price could fluctuate upwards by any amount.

## How we talk about risk & my pedantic point

Let's return to the quote above:

```
Shorts are a more risky investment because they have infinite risk.
```

You can see exactly what I summarized [here](https://www.investopedia.com/terms/u/unlimitedrisk.asp). 

This is all largely rubbish and perfectly illustrates how poorly we (humans) think about risk and, tangentially, large numbers.

What would have to be true for a stock short to be infinitely risky? *The stock would have to go to infinity.* I'm not even sure what that would mean in this context -- a stock so valuable that everyone always wants it forever at a price greater than all money that exists? What would this company produce? Immortality? God?

My cursory Googling shows [Berkshire Hathaway stock class A](https://www.marketwatch.com/investing/stock/brk.a) as the most valuable stock in America at $405,164. Ignoring splits, say you shorted BRK.A early when it was at $20. You would be out at $405,144 dollars. This is *not* an infinite amount of money. It is $405,144 dollars.

What's more, in order for it to become infinitely risky, the owner of the short also has to hold it to infinity. If you've decided that you're going to exercise your short position when it loses a maximum of $10 and act on that, then the risk is not infinite. It's capped at $10. Of course, people are certainly *bad* at doing this, but people also don't like to lose lots of money in perpetuity.

I know this is pedantic, but we need to stop talking about shorts as if they are always going to infinity. They aren't. We know this by doing just back-of-the-napkin math and looking at the basic assumptions of those words.

 This reminds me a lot of [Big O notation](https://en.wikipedia.org/wiki/Big_O_notation) in Computer Science. A well designed hash table functions in O(1) complexity in practice, but still has a O(n) in theory because there's the possibility that everything got jammed into a single entry in the hash table. This never actually happens of course, but mathematically, hash tables are still labeled as O(n).

Shorts are the same way. They aren't infinitely risky, but we label them that way because mathematics dictates that *theoretically* it can go to infinity. Reality is a lot messier, though, and most things fall into the middle ground. 

In short (haha), this is really how we should summarize a short risk profile:

```
Shorts are a more risky investment because they have an unknown downside potential.
```

Use shorts with caution and set limits that you stick to, and shorts are a totally fine investment tool.
