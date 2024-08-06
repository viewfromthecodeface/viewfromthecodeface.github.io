---
title: "Programming: It's all storytelling"
date: "2017-03-08"
categories: 
  - "stories"
coverImage: "stories-around-campfire-crop.jpg"
---

Whilst programming is thought to be a purely technical field, it isn't. People are far more important. And that means we have to get our ideas across to other people clearly, whether in code, in a sales brochure or in a video.

And the way this has always been done best is by _**telling stories**._

But how does that relate to code?

<!--more-->

_"It was a dark, crisp night. As the flames cooled, our conversations warmed. What would tomorrow hold? ..."_

**Stories**.

They have been with us since the earliest times.

Campfires. Hieroglyphics on caves. Parents passing on life hacks to their children.

Humans are intensely relational creatures. Even those of us who rather like to sit in front of a laptop all day.

Stories connect us.

More than dry facts, we get a sense of others. What they hope for. What they fear. What brings them joy.

But what has all that got to do with software development?

## Programming is storytelling

As a beginner programmer, like most of us, my code was a completely mess. No thought of structure or form, as I hadn't learned that yet. I was just happy if it worked.

I've made programming interns almost weep with frustration at my ball of mud.

As I progressed, and started to work on code I had not written, I learned how hard code can be to read. Taking my first role leading a dev team, I saw how hard it was to _explain_ unreadable code.

I mean, what does this code do? :

\[code language="java"\] t += o.cst(); if ( o.comp() &amp;&amp; o.dis() &gt; 0.0 ) { t -= o.dis(); } \[/code\]

Beats me, too.

Yes, there some familiar keywords. There are _almost_ recognisable names. But ... It's like looking through a grimy mirror. Seeing but a dim reflection of what might be.

**This code tells a story,** but it's a tale of a programmer who isn't telling one. A programmer who got the job done, perhaps, and made things work. But then hid the evidence from future explorers.

It may even tell a story of deliberate obfuscation. Perhaps a lack of care. Perhaps a toxic culture of "compressed deadlines", or poor training.

But the story it tells me is that _this code will be hard to change._

## What's wrong if it works?

So what exactly is wrong with the above code, assuming it works?

For me, it doesn't answer the big picture questions:

- _What will happen after this code has run?_
- _Why is it here?_
- _Which part of the application does it make work?"_

It's full of detail without context. It hints at having names, but you can't be sure what those names mean. You can see if has a conditional. But what is it there for? When our customer asked for "that thing they needed doing", which part do these lines play?

When you are _writing_ code, you can gloss over all this. In that moment, it is obvious.

But when you are _reading_ code, all that context has gone.

## Intentional code tells better stories

But what if we see the role of computer code differently?

What if we treat it _not_ as some shopping list of orders written to a CPU.

What if we treat it as being written to a _human_? 

How about we **write code to tell humans what the computer happens to be doing?**

It's a significant shift. Let's try it:

 

\[code language="java"\] private double calculateTotalPriceIncludingDiscount( Order order ) { double totalCost = 0.0;

totalCost += order.getCost();

if ( isEligibleForDiscount( order ) ) { totalCost -= order.getDiscountAmount(); }

return totalCost ; }

private boolean isEligibleForDiscount( Order order ){ return order.getDiscountAmount() &gt; 0.0 ; } \[/code\]

With this simple refactoring, this code tells a clear story.

It is code to get the total price of an order, for our eCommerce site. This price includes any discount that we put against that order.

We have used several intention revealing techniques to tell our story:

- **Descriptive variable names** The names tell us what the variable is used to hold, not its data type
- **Descriptive method names** The method names tell us what this method does, overall: Why it is there
- **Explanatory methods** We split out a method isEligibleForDiscount() to explain why that conditional was so interested in the discount amount
- **White space** Human minds chunk information. White space guides our eyes to the chunks we have designed

### This is bigger than you might think

A few small changes? Made the program even more wordy? Had to type even more letters?

This may not seem like much of an improvement.

_But it is massive_.

Come back tomorrow and re-read the two code examples.

You will notice that the second one tells its own story, clearly. The first one, not so much. I mean, we can both guess. But guessing leads to mistakes.

As your code size grows, as people leave and join the team, as the feature turnaround picks up speed - these are the little things that will keep you afloat.

Clear code means less bugs in new features.

Clear code means new developers can read the code and be clear what you meant it to do, alone.

Clear code compounds. Each new piece of code, kept clean, becomes a more powerful tool, able to be used and understood by everyone.

## Interviews are storytelling

It's not just coding where we need to tell clear, intentional stories.

Your C.V. and the way you present yourself in an interview tells a story about a product to a potential buyer.

That product is, of course, _you_.

Imagine this.

You were prevented from attending a job interview. Somebody else turned up to represent you.

Here's what they were allowed to do:

- Code in their own way, and say that's how you would do it
- Speak to the interviewers however they liked: Politely, disinterestedly, timidly, confidently, arrogantly
- Dress how they liked
- Use a tailored CV, or just send out whatever was to hand
- Fill up a Google search on your name with whatever tweets, photos, youtubes and blog comments they wanted

_They could tell any story they wanted to about you._

You would hope they wouldn't present you in an awful light.

You would hope they knew the best about you, and could explain, honestly, why you might be a good choice for that role.

_But of course - they don't exist. They are you._

Each of us gets to choose all these things.

We choose the story trail we create in our lives, long before an interview.

We choose not only what we say, but how we say it during the interview. We choose what kind of code style we present. What way we work with others.

Every interview gives someone else the chance to build _their own story_ about _you_.

It's up to us to help them choose the right one.

## Marketing is storytelling

The number one reason for product driven companies to fail is that they don't sell any of their products.

As developers, we can get a little isolated in our thinking about marketing.

It seems perhaps not our job, our something we would rather leave to others.

But it actually an extension of how we get our code to tell stories.

Our products tell stories.

To potential customers.

And these human beings, who decide whether or not to buy our code, inside that product, and keep us paid - they form a story in their minds.

It's a story of the future. And how their life will be changed, once they use your product.

It has to appeal to them in some basic way. Will I be richer? More popular? Attain the status I want? Be entertained and laugh? Be inspired? See the last of that tiresome problem I have today?

All marketing involves finding humans who your product can help, and then finding out the story of the future they want. The product design and code has to then make that happen.

Apple users love elegance, simplicity and style. You can see that the code behind an iPhone's user interface brings those very qualities to life. A fast, smooth, swipe effect allows the users to feel that they are not just using a smartphone - but they are doing it with style.

And that product feature - like all features - starts off with we developers making code to make it happen.

In startup land, we might ourselves need to get involved with marketing, like I did.

But even if we don't, remember that our code defines what story our product is able to tell. And that's important.

## Case studies are storytelling

Trust is a funny thing.

Hard to earn. Easy to burn.

Part of marketing is "pushing people over the line".

You'll know this yourself. You get interested in a product, decide you more or less want it - and then freeze.

What if it doesn't do what I hope it will?

Everybody experiences this, and so a distinct part of a sales funnel is addressing concerns.

A good online way to do this is with a Case Study.

A case study will tell the story of why a customer chose your product over others, what it now helps them do, and gives them a chance to confirm it really works.

Because humans buy our products, we like to see other humans directly for this. A chat over coffee with a trusted friend is ideal.

Failing that, video is a great medium for telling stories, case studies being no exception:

https://player.vimeo.com/video/1802901

(video production by the very talented [Greek Bloke Productions](https://vimeo.com/user690354))

I really enjoyed the whole process of creating case study videos, presenting, interviewing, setting up the tech kit. It's brilliant to talk to people, and moreso when they are saying nice things about a product you care about!

But whoever does them, it's good to recognise that they are human stories at heart.

## How do we tell better stories?

I've no idea how you would write a fiction novel, or a script or a screenplay of any size. But I have tried to learn how to tell simple stories clearly.

- Remember - you are writing to be read by a human
- You have ideas in your mind, now, that you want another human to have in their mind later
- Make your intentions clear
- People see things through their filters, experience and prejudices. Allow for that
- Humans like overviews and context before masses of details

As we get more involved in software, and the businesses around our code, our ability to tell stories is a huge advantage.

 

_main image credit: https://www.flickr.com/photos/jkirkhart35/4984385396 with changes (see [licence](https://creativecommons.org/licenses/by/2.0/))_
