---
title: "Out of the box ideas? Here's three that paid off"
date: "2017-03-23"
categories: 
  - "stories"
coverImage: "EPROM-Microcontroller_Motorola_MC68705_1.jpg"
---

Most times in software development, we like our processes.

It's nice to know that the web app you've just set live actually works. So we have a few processes around writing tests, and hiring QAs to make sure that happens.

But sometimes, the best results are found when you do things a little more creatively.

### The One Second Cache

Our small team was building the company's first 'Enterprise Java' application. It was a networked systems monitoring and alerting product.

Normally, the company would have used C++ for this job. But this was 2005. And the whole Java/Spring/Hibernate/Tomcat ecosystem just seemed too good to refuse. So we pitched stakeholders to make the switch.

As you can imagine, this caused a bit of consternation. Any new technology direction is a risk. Could we do it? Our little team? Why us? Why now?

And we were asked the dreaded _'but isn't Java terribly slow?'_

We made very good progress with our fledgling app. We had useful features out in a few weeks. This was just as well: we had to do a live webinar demo in three days time.

It's no surprise to any developer that the word 'live demo' had its traditional effect. With hours to go, we made a change - and our app slowed to a crawl.

Click a button .... wait ..... wait .... did something just change?

This was not the best news. We needed at this first demo to get buy-in from those concerned about speed.

Pizzas ordered, another 11pm work night and we debugged our way to the cause. Configuration files. Our app was reloading configuration data thousands of times per request. And each time caused a fresh file read.

So we added a cache.

And that's when we went down the developer spiral of doom arguing about how long to cache things for. In production, this data would never change. In development, we often changed it. So should we store it for an hour? A day? A week?

My colleague ended up with the right answer. _One second_.

I was sceptical. Because I had misunderstood the problem.

In my mind, we had to _optimise_ how often we loaded the data - to do this as infrequently as possible.

But this was a problem we simply didn't have.

By storing it for a single second, only the first of the thousand-plus accesses in a web request would cause a file read. And that gave us instant response times.

_By viewing the problem in the right way, we used a surprising solution to great__effect_.

### The High Priority, Low Priority Interrupt

Whilst the Internet of Things (IoT) is all the rage, industrial control systems have been around for decades.

In the 1990s, the Siemens team I was part of developed a Profibus DP controller to connect together pieces of factory machinery.

Profibus, you can be forgiven for not knowing, is a specialised high-speed networking system, deisgned for industrial environments. It really is quick for its era. One of the hard real-time constraints was that a signal on the network cable had to be processed within microseconds. On our Siemens C165 16 bit CPU, we had enough time ... but only just, with careful design.

The familiar theme of 'we need a live demo' cropped up. Predictably, the day before, we noticed something less than stellar.

The communications worked fast and reliably. But the device we were building had a seven segment LED display on it, for human operators. And it flickered like an angry fluorescent wasp in a jam jar.

It wasn't wrong. It just looked like we didn't know what we were doing :) If the most visible part of the system looks to be struggling, why would you be confident that the product worked?

We knew it would be wrong priorities in the real time concurrent code. When a network packet came in, it caused the display to not update by locking the CPU.

We spent ages tinkering around with real time operating system priorities, but without luck.

And then I stumbled on a great hack. I set the display code to be the highest priority thing in the system. It was higher priority than the mission-critical networking code, with its tight hard-real-time deadline.

You know that curious, sideways look that colleagues give you sometimes, when they think you've lost it? That.

_But it worked_.

I knew the conventional wisdom was that the mission critical thing gets the highest priority. But I also realised that our display code took so little time, we could fit both it _and_ the mission critical code in. Worst case, we could guarantee to meet the deadlines.

Flickering stopped. Nothing to see here. Just a neat, professional looking system.

_It's easy to fall into the trap of 'doing things right'. But it's not always 'doing the right thing'._

### It's cheaper to throw it away

Do you remember these?

![](images/AAEAAQAAAAAAAAeuAAAAJDA2MWRkY2UwLTc5YWQtNDUxOS05YjZlLTg4ODhlZTI0MmJmOA.jpg)

That's an Ultra Violet light EPROM eraser. With a drawer full of EPROMs. Allow me to wipe away a nostalgic tear ...

In small embedded systems, the code doesn't usually live on a disk drive. It either lives inside the CPU, or some external Read Only Memory (ROM). EPROMs are memories that can store code, and can also be erased by UV light.

That lets us coders make changes. And that's a good thing, because sometimes we get the code wrong. Changes are very handy then.

During development of Siemens 6SE21 variable speed drives code, I would routinely make a code change, burn it to an EPROM, and then swap the chip on the board. The old one would go and have a little sunbathe in the UV eraser.

This took a couple of hours to complete. We had a few EPROMs to rotate through.. but not many. We were a big company dev team, but we weren't daft when it came to spending money.

So I thought I would buy some more. And I noticed an interesting thing in the catalogue (pre-web days).

_You could buy one-time programmable chips for a fraction of the price_

This was unexpected. The whole point of a re-usable memory chip is to keep the cost _down_, right? And yet simple sums showed that buying several tubes of one-time chips would be cheaper, faster and better. It would also save hours of my time, which came at the loaded labour rate of a senior developer.

Just burn the code, swap the chip, and bin the old one.

_Again, confusing 'what I thought I should think' with 'what is actually best' was wasting time and money_.

 

I no longer do embedded development, being firmly in the world of web and mobile apps. But I still try and look out for a better way to do things - even if it's not the accepted 'best' practice.

 

### Image Credits

Many thanks to these kind people, who are handy with a camera:

- _[http://www.flickr.com/people/63794141@N00](http://www.flickr.com/people/63794141@N00)_

(article originally published on [LinkedIn](https://www.linkedin.com/pulse/three-surprising-things-software-alan-mellor))
