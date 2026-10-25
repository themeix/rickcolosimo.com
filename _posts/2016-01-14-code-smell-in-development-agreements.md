---
layout: post
title: Code Smell in Development Agreements
date: 2016-01-14 08:31:35 -0400
author: Rick Colosimo
permalink: /code-smell-in-development-agreements/
excerpt: Code Smell in Development Agreements I recently answered a Quora question
  about the Gigster contract for freelance developers. In that answer (reproduced
  below), I run through some basic considerations that almost always deserve attention
  – regardless of whether I’m representing the developer or the client. If you read
  through the comments, you’ll see a number…
categories:
- five-minute-lawyer
tags:
- drafting
- software-development
---

Code Smell in Development Agreements

I recently answered a Quora question about the [Gigster contract for freelance developers](https://www.quora.com/Is-the-contract-for-Gigster-reasonable-for-the-developer/answer/Richard-J-Colosimo). In that answer (reproduced below), I run through some basic considerations that almost always deserve attention – regardless of whether I’m representing the developer or the client.

If you read through the comments, you’ll see a number of problems (undeclared variables (Statement of Work; Company), two variables for the same reference (Company; Gigster), non-DRY language (Section 2.3’s duplication), and unrefactored language (drafting throughout; disconnect between Gigster and Customer acceptance of Deliverables). As I’ve described them above, they will probably sound a lot more familiar to you than they would if I used legalese to describe them – but of course, people who speak in legalese seldom identify these things as problems.

On the other hand, I prefer to write clear contracts that cover the necessary ground – what happens under scenario A, scenario B, and then under all the rest. That way, whether you’re a developer or a company having software developed for you, you can understand what is expected of both sides, with clarity about rights and obligations.

> Good fences make good neighbors.

Robert Frost’s “[Mending Wall](https://en.wikipedia.org/wiki/Mending_Wall)”

Having been a litigator early in my legal career, I’ve learned that the most important thing about contract drafting is that if the answer is “well, then you get to sue them for that,” you have no answer. The out-of-pocket costs of a lawsuit are literally easily $25k–50k, and the distraction and lost opportunity are probably just as much. You are dramatically better off avoiding lawsuits.

Some lawyers believe that the path to advantage is in writing terribly one-sided terms (like the assignment below of other “inventions” that don’t constitute deliverables) and then fighting tooth and nail over every clause: this is the stereotypical NY big law firm approach, and I know how to do it like just about every other [Ivy League](http://lawschool.cornell.edu) lawyer.

However, I learned in Silicon Valley that a much better approach is to do the “right” deal for the client as quickly and smoothly as possible. As a practical matter, the real risk in a transaction is from operational risk, not a hypothetical risk from two different versions of something that’s not supposed to happen (like arguing over provisions following the default of the United States on government bonds).

I seek advantage in defining the risks you’re willing to accept and clarifying what you’re demanding in return for taking on those risks for the other party. Writing clearer language that is harder to misconstrue reduces the costs of disputes and reduces the chance that you’re going to court. With that leverage, it should help you negotiate your way out of a problem, which is almost always a dramatically better solution than going to court.

---

> If I were representing, as I do in other contexts, a software developer or firm that was taking on an engagement through Gigster, I would have a few significant comments.  
> In general, the Gigster agreement is typical in form, meaning that it has unclear language, defined terms that aren’t defined, and some clunky spots. Keep in mind that Gigster may or may not be interested in updating the base agreement or creating a side letter amendment for a specific project.  
> Here are some specific comments and observations I would raise with a client:
>
> 1. Section 2.1 – the assignment of deliverables is fine, but the assignment of all other inventions that “arise in connection with the Contractorervices … including … source code developed or created by Contractor that is not specific to Customer and is generally applicable to other Customer projects and deliverables ….” seems overbroad. As I read this, if DHH were working on a webapp for Gigster, they would claim ownership over Rails. That seems aggressive.
> 2. Section 2.2 exempts pre-existing IP of the contractor from the assignment, but the language in this section purports to limit it to pre-existing IP that is disclosed in writing to Gigster before the delivery of the Deliverable. It might contemplate that before such items are included or as they arise, they are disclosed to Gigster on a rolling basis. In any case, this requirement would require some integration into a developer’s workflow.
> 3. Section 2.2 also grants a license to use any Contractor Technology in or needed to the deliverables or other inventions, meaning that a developer would not want to use any “real IP” in the course of this agreement; in many cases, a developer would want to prepare a standalone license agreement to monetize that IP or more strictly limit its automatic licensing.
> 4. Section 2.3 has a lot of duplicative language about assignment that doesn’t seem to apply to a waiver of moral rights.
> 5. Section 2.4 requests written permission but doesn’t clarify from whom. It’s probably meant to be the third-party licensor because Gigster is mentioned in the first sentence, but it’s not clear. Is it the customer? Maybe it is Gigster.
> 6. Section 3.1 says the developer (unless it’s milestone-driven) gets paid after “acceptance of the Deliverable by Gigster.” But Section 3.2 sets up a clawback if the Customer rejects the deliverable. In any case, there’s no description of any acceptance process. This is non-standard and a common source of problems for developers and clients alike. Maybe it’s on the project page, but that’s not mentioned here. There should be a formal acceptance procedure and timeline after which objections are waived and a deliverable is deemed accepted.
> 7. Section 4.1 is silent on whether Gigster has any payment obligations if it terminates the contract without cause. Typically, some percentage of completion measure is used. This term would cause many developers to either only use this for small projects or to elect milestone payments to reduce their risk. There’s no mention of upfront payments or deposits, so those common methods of reducing risk seem to be unavailable.
> 8. Section 7.2 uses the term “Statement(s) of Work,” but it’s not defined and does not appear in the terms of service. Maybe it appears on the Project Page.
> 9. Section 7.2 requires that no open-source code be used. It’s broadly defined, and so even sample code found on stack overflow might be implicated. (An argument that many would make is that there are no damages from a breach of that provision if the code in question is unremarkable and perhaps indistinguishable from independently written code. But who wants to fight over this?) The same is true for any code with a GPL-like license that requires licensing of certain derivative works. On its face, this provision would seem to rule out a rails project, and the no third-party code would seem to rule out apps incorporating SDK code without specific permission from Gigster. Hopefully they incorporate those permissions in the project page and specifications.
> 10. Section 8 requires indemnification of Gigster by the developer for infringement. However, it extends to all “Inventions,” which includes things not included in the Deliverables (for which indemnification is typical). If a developer invents something, that Gigster takes, that turns out to have been patented by someone else the day before, the developer is now on the hook even though the developer didn’t get paid for that invention or make any intentional distribution of it to the customer or Gigster. I think it’s overly broad and outside the typical scope of an agreement like this.
> 11. Section 10 – the non-solicitation is overly broad because it includes contractors and there’s almost no way to find out whether someone falls into that category. It doesn’t include a common safety valve for general, non-directed advertising. Also, the developer can’t work for any Customer without Gigster’s consent. This section uses “Company” as a defined term that is not defined. It’s almost certainly meant to be Gigster but still….
> 12. Section 10 also says that a contractor can perform other work unless there’s a “conflict of interest.” That’s not defined and overly vague. Presumably every freelance developer has an inherent conflict of interest with Gigster because they compete with each other.
> 13. Section 11 contains a typical arbitration and no-class-action clause. It’s worth noticing but not unusual.
>
> Of course, each of my clients has particular concerns that are unique to them, so this list alone wouldn’t be sufficient to give them advice about any particular engagement. If you’re reading this, these questions may or may not be significant for you, and they almost certainly don’t capture all your issues. Real legal advice deals with your specific facts. Don’t get caught by not getting the real answer.
