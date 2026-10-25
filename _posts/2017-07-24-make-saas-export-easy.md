---
layout: post
title: Make SaaS export easy
date: 2017-07-24 08:33:59 -0400
author: Rick Colosimo
permalink: /make-saas-export-easy/
excerpt: It’s not one SaaS app to rule them all, no matter how cool you think you
  are. And if there is one, it’s probably not yours. (It’s probably Gmail.) I get
  that you think your app is the cat’s pajamas and that not only will no one ever
  want to use anything else, but that…
categories:
- general
tags:
- customer-focused
- saas
- standards
---

It’s not one SaaS app to rule them all, no matter how cool you think you are. And if there is one, it’s probably not yours. (It’s probably Gmail.)

I get that you think your app is the cat’s pajamas and that not only will no one ever want to use anything else, but that they also *should* not. And so you don’t build in an export function. It’s for their own good, you say.

But it just ain’t true, like a corollary to “[Jakob’s Law of the Internet user experience: users spend most of their time on other sites.](https://www.nngroup.com/articles/fresh-vs-familiar-aggressive-redesign/)”

Do us all a favor: throw in a CSV or Excel export, since both of those are typically readily portable to other solutions. JSON is less helpful as an export because it’s harder to import your JSON unless someone has built an import specifically for your format. CSV and Excel are also more user-friendly because someone can crack it open and probably figure out the structure and tasks in short order. JSON might be workable if you have a nice parser in Chrome, but to the average user, it’s incomprehensible. (To me, it looks like C circa 1986, with all the damn indents and braces.)

Why should you build in an export? For one, it’s about being a good internet citizen. What do I mean by that? I mean that the reason email is a killer app that dominates twitter and slack and ICQ and BBM and pretty much everything else is that it’s standards-based and you can relatively easily move your stuff from one provider to another. Switching clients for email is nearly trivial if you know what you’re doing and not terribly difficult if you don’t.

Using different calendar clients is also not that bad, if you understand where your calendar data is or understand what an ICS file will do for you. V-cards are still awfully damn messy, and no one seems to have a clue how to keep my contacts in order. I’ve found, over the years, exactly 1 contacts tool that does what it says and does what it should: copy2contact. It’s an app that probably hijacks my phone and dials directly to the Kremlin at this point, it’s been so long since it’s been updated. I used their outlook plugin years and years ago (that tells you how long ago it really must have been): you copied some text, like an email signature, to the clipboard and it turned it into a contact entry. Before that, nothing did a good job since planetall.com. I’ve spoken of my sadness on that front before, so I won’t repeat myself.

Tasks: please. everything’s a damn mess. There is a tiny bit of organization arising around taskpaper formats for plaintext tasks, but everything else is running like we’re doing email in 1953 before someone had the sense to write an RFC (and no, I really have no idea when the original email standards were created, but I’m guessing there were incompatible message systems before that). The standard made a big difference. Think about the fortunes made in email: hotmail, gmail, outlook, and I can’t even imagine how many other clients were built, launched, and sold. The standards made that possible.

So, back to the beginning. Maybe your app isn’t really part of a standard, but maybe it could be. Maybe you could work to provide more value to your customers by giving them an option to get their data out (perhaps a bit simpler than an API or a Zap, please?). Maybe you could start to design and frame the standard so that more people can, and want to, do what you do.

If the data’s already in a database, are you really going to tell us it’s too hard to figure it out?
