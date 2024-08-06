---
title: "Programming: It's all about the people, not the language"
date: "2017-03-23"
categories: 
  - "stories"
---

A great question over on [Quora](https://www.quora.com/Why-do-Java-programs-end-up-being-longer-to-write-than-the-equivalent-Python-programs/answer/Alan-Mellor/comment/32473253?__filter__&__nsrc__=2&__snid3__=864806894) (thanks Khalid!)

> Why do large corporations (e.g Quora) decide to write their important applications in python when they know that as the complexity of their code base increases, figuring out the interacting components will be hard?

It’s a great question, and it’s taken me 30 years to figure it out.

<!--more-->

## How large software systems get built

Programming a large system has a flow.

It starts off with one or two people with an idea. A small system is then built. The system grows in size and complexity. The team grows in size and complexity. The small system gains traction in the market, and users demand it goes in a different direction.

At each step, the programming is dominated by human choices.

That first system, with those two coders - what is their favourite language? Because that’s the one they will pick. Is there any existing code to speed development? If so, then that might steer the choice to another language. As an example, the existence of the OpenFire server, plus staff expertise made Java the clear choice for building yuuguu.com

## Growth and the hiring circle

The larger project - well, now we are hiring people.

We can only hire people who are available. And these people are professional programmers. These people like to stay employed, and so learn the most "popular" languages. The ones with the most job adverts.

So you can only easily hire for popular languages. It forms a virtuous (vicious?) circle.

But by this time, the codebase is already up and running - in its first language.

Do we re-write, and lose our investment? For the dream of “better development”?

Most likely, we carry on. We might add a new additional system in other languages, but rewrites are rare.

At the large system end, it doesn’t really matter anymore.

## Systems in the large

Execution speed is dominated by scaling, algorithms, data schema and overall program design.

Development speed is dominated by readability of the existing code.

When I started out, I figured it was all down to ‘pick the best language and you’ll be fine’.

I now know it’s all down to people.

_People issues dominate development, not language._
