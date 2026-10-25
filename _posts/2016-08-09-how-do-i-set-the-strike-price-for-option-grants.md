---
layout: post
title: How do I set the strike price for option grants?
date: 2016-08-09 12:30:51 -0400
author: Rick Colosimo
permalink: /how-do-i-set-the-strike-price-for-option-grants/
excerpt: 'When the board makes option grants, it has to set a strike price – the exercise
  price for each option. (NB: this applies equally to stock options for corporations
  and unit options for limited liability companies, so don’t get thrown off by the
  terminology.) How does the board do this? You look at the plan,…'
categories:
- five-minute-lawyer
tags:
- stock-options
- taxes
- valuation
---

When the board makes option grants, it has to set a strike price – the exercise price for each option. (NB: this applies equally to stock options for corporations and unit options for limited liability companies, so don’t get thrown off by the terminology.)

How does the board do this? You look at the plan, which probably tells you that the closing price of the stock on the exchange is the price.

Oh, you mean you’re not a publicly traded company? I guess this post will be longer than originally planned.

1. The first step is still to look at the option plan. It will include any of a few typical restrictions, such as the exercise price must be at least fair market value (FMV) or the exercise price for certain grants must be at least 110% of FMV. It’s almost alway permitted to have an exercise price that is in excess of FMV.

We’ll come back later to the question of why the FMV trigger is so important, and we’ll also discuss why companies typically grant options instead of just giving outright equity to the grantee. (Spoiler alert: taxes.)

Setting the strike price means identifying the FMV of the share that is subject to the option. Options are typically common stock, so if there isn’t a complex capital structure (meaning one or more series of preferred stock), then most boards start with the value of the company and then divide to get the FMV of a single share on a fully diluted basis. (You can see how that math works by experimenting with my [financing spreadsheet tool](/tools/preferred-financing-calculations/).)

1. This makes the second step figuring out the value of the company.

For early stage startups in the pre-seed world, there’s little science to the effort at this point except that you want to ensure that the price is equal to or greater than the fair market value today (to avoid unpleasant tax consequences for the grantees). If the company has a financial model that you’ve used to build a valuation (perhaps using a tool like [Thoughtstorm’s](http://thoughtstorm.com) [simplified valuation model](http://www.thoughtstorm.com/tools/simple-valuation-model/)), then that’s your starting point. (You can read more [than you need] about [valuation approaches](http://www.thoughtstorm.com/bolstering-valuations-through-detailed-analysis/), too.)

As the company’s capital structure becomes more complicated, the simple method doesn’t necessarily work well to get the “true” FMV. Liquidation preferences for preferred equity will reduce the net value of the common equity on a sale, so a straight division (company value/fully diluted capitalization) won’t work.

1. This makes the third step figuring out the value of the particular security (stock or unit) that is the subject of the option.

At this point, companies take one of two approaches. If they have other reasons for wanting to get closer on the valuation, they might engage a consultant to do what’s called a 409A valuation. That type of valuation, typically used to avoid tax penalties on deferred compensation, usually values each class or series of the company’s equity. Historically, companies would grant options at 10% of the price of the most recent preferred financing, and as the company got closer to an IPO, they would increasse that percentage (since at the IPO, the prices essentially converge). Some tools that are designed to reflect this approach (but that I haven’t been able to investigate thoroughly) include [vcAdviser](http://www.vcadviser.com/index.php/services/). So there are options short of a $5000 outside valuation.

The second approach? It brings us back to my point about why FMV matters.

The IRS treats the issuance to a person of a share of stock to be income to the extent that the price paid for the share is less than the fair market value. If you give the employee a $20 bill, that’s income. So far, so good.

But what If you give the employee the right to buy a $20 bill for $10? The IRS treats that transaction as $10 of current income recognized *at the time of the grant of the right*. The same analysis applies to a share of stock (or unit of an LLC). If you give the employee the right to buy for $0.25 a share that is “worth” $1.00, the IRS sees $0.75 of **taxable** income. That’s a major reason why granting options below FMV is an anti-pattern: it creates unpleasant tax consequences. Imagine: you grant a new employee 100,000 options at $0.01, trying to be generous, when the FMV is $1.00. Without any regard to vesting, the fact that the option hasn’t been exercised, the fact that the option securities haven’t been sold, or the possibility that the FMV might go down in the future, the IRS will see $99,000 of taxable income and require your employee to write them a check for about $40,000 (state and federal; YMMV) of real money to pay taxes on the paper profits. Let me give you a #protip here: employees really hate that.

The situation is the same but worse when you grant equity. Then, the $0.01 strike price isn’t even deducted because the IRS sees “here’s something worth $20” as the equivalent of “here’s $20” and taxes it accordingly.

In fact, this “pay taxes in cash today on non-cash ‘paper income’” problem is why option grants exist. Option grants are “you get the right to buy this rare coin, worth $20 today, for $20, and you can have that right for 10 years.” The IRS evaluates the present right at $0 and an employee can typically avoid taxes until the grant is exercised. (NB: Section 83(b) elections make this annoyingly complicated and unnecessarily tricky. Future post material.)

So, to bring us back to the second approach, this seemingly lopsided application of tax liabilities leads many companies to simply accept that the simple valuation method makes an error in the value of the option, yes, but in a way that is less detrimental to the grantee than imposing a cash tax obligation on paper income.

Many startups will then take the cash-efficient route of taking their valuation, dividing it by the fully diluted cap, and accepting that the strike price might be higher than FMV.
