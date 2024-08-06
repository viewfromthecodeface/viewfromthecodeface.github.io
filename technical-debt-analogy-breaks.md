---
title: "Technical Debt: Where the analogy breaks down"
date: "2017-03-22"
categories: 
  - "stories"
coverImage: "tech-debt-title.png"
---

I’m a big fan of Martin Fowler’s definition of technical debt, [here](http://martinfowler.com/bliki/TechnicalDebt.html).

The name refers to the myriad ‘‘do it quick, or do it right’ decisions made by engineers everyday. In software, we have a little more freedom than our friends in Aeronautics to actually ship something that works - but only just. We can always fix it later. With a 747 - not so much.

But just how well does this analogy fit typical software projects?

<!--more-->

Fowler defines Technical Debt so that it is familiar to the accounts department. It is the idea that _some debt is good_. Home buyers take out mortgages - debt - to buy a house. Business owners take out a loan, or VC funding - debt - in order to scale out a business.

These are good uses.

Bad uses include taking out a £500k personal loan to blow on a monster party. Long after the last broken glass has been swept away, you will still be liable for the loan plus interest. With nothing to show for it. And no asset you could sell to raise the repayment.

Technical Debt in software is then pragmatic choices to ship software to a hastened deadline, to gain traction or book revenue early in some way. Out of the profits, we can go back and ‘pay down the debt’: rework the software to get it right.

The analogy, whilst helpful,  breaks down in two important ways.

**Non leveraged Technical Debt**. Like our ‘loan for a party’ example, this is where the debt has no lasting benefit. Now, we’ve had a name for this in software for a lot longer: bad code. It is all too tempting as an engineer to call all my bad code ‘technical debt’. It isn’t.

**Paying Down without Cash.** The most serious breakdown is in how we pay down the debt.

A real debt is paid with cash. Cash is a form of universal barter. It was invented to solve a specific problem. If I have a goat and want a hair cut, and you are a barber who wants a goat, we can make a deal. Cash solves the problem that happens when you don’t have any use for a goat. Or I think that a hair cut is worth less than a full goat.

The analogous problem in software technical debt is that we can pay down the debt if we can easily reverse the work we did - the ‘haircut for a full goat’ scenario.

Typically, this is wishful thinking. Software moves on.

In large teams, as soon as I check in my ‘debt’ code, other programmers will download what I have done, and then _build their code on top of mine._ The assumptions I intended to be temporary now must become the basis for the next phase of development.

Technically, this causes software couplings to my variables, data structures and APIs. It also causes the more insidious problem of connascence. For example, my technical debt may be that I - hideously - used a ‘magic number flag value’. So a person’s age might range from 0 to 200 years, and then I use 201 years to mean ‘person’s age not known’.

The next programmer might (?) find a handy use for this, and write code that assumes unknown ages will always be set to 201. They might do something equally hideous like start a loop at 201, counting down to zero in a bid to find a maximum age.

It is an artificial example. But can you see how - now - my technical debt has become locked in to another part of the system. Now another programmer refactors all of this, preserving behaviour. The magic number becomes even further entrenched, and changed to a new and more centralised form.

When I come to paying back the technical debt, I find that it is no longer a case of removing the magic number code. I have to _find_ that code - in its new form - now it has been refactored. I need to understand if removing the magic number will now _break_ the code built on top of it. This code may now itself be in production - or, worse - have become a published API specification that third parties rely on.

All of a sudden, I can no longer pay down the debt using the same currency.

In software, we have no cash equivalent. There is no universal set of lines I can type to fix the problem. Each downpayment is custom and unique, not universal and transferrable.

In real world debt, the amount might go up, but at least you just need ‘more of the same’ to repay it. In software, you quickly get to a point where the repayment becomes impossible.

Just an observation. Let's not be too quick to talk about 'technical debt' without realising that it's not always simple to fix it afterwards.

 

* * *

Originally published at [LinkedIn](https://www.linkedin.com/pulse/technical-debt-where-analogy-breaks-down-alan-mellor)
