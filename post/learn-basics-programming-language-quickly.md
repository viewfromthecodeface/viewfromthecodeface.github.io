---
title: "How to learn the basics of any programming language quickly"
date: "2017-03-13"
categories: 
  - "tips-and-tricks"
coverImage: "programming-languages-wordcloud.png"
---

As a commercial developer, you end up programming in a variety of languages.

I've used C, C++, Java, PHP, JavaScript, PLM/51, a ton of 8/16 bit assembler languages, Pascal, FORTRAN, BASIC.

A common beginner question is '**How do I learn so many languages?**'

And the answer is, of course: _you don't_. You get good at picking up the basics as you go along.

Here is how I do it: I learn the three basics of any language.

## Learning the three basics of any language

Getting fully up to speed with any language - and all its IDEs, libraries and idioms - takes time.

But you have to start _somewhere_. And thankfully for us, all current languages support the three basics:

- Variables
- Conditionals
- Loops

### What are variables?

You know how you might make a shopping list, and say you would like three apples one week, but hen change your mind  next week and only have two apples?

You can think of that as varying the number of apples you want.

That's what **variables** are for.

Without variables, every single difference to your shopping list would need a new program written.

Every language has variables. And each language has its own way of coding them.

### What are conditionals?

Ever been in a shop, seen a magazine you quite like, and thought "_I'll buy it if it's less than a fiver?_"

That's a **conditional**. You will do something _as long as_ your condition is met.

Programs need to do this - because, always remember, programs exist to automate what people can do.

### What are loops?

Loops are the production line of programming. Think of making cars. Each one needs the steering wheel fitting to it. As soon as one is done, the next car rolls along and we do the same thing again, on a different car.

This is a **loop**.

Programs use loops to apply the same program logic to different variables. Or just to do the same thing over and over again.

## Let's learn C programming in three steps ...

Here is my "all purpose learn the basics fast" method to get started on a new language.

Let's pick the C language to practice on.

But do understand that these steps - finding out how to code each of the mini programs in your new language - applies for all languages.

### Preparation: How do you make a program run?

Before doing our three steps, we must first find out how to make a basic program run.

Every language has its own ‘code you just have to write’ to make the program run from the operating system.

Traditionally, we make our first program write Hello, World to the simplest thing it can write to, like the console.

For C, it is

\[code language="C"\]

#include &lt;stdio.h&gt;

int main() { printf("Hello, World!"); return 0; }

\[/code\]

Get that to compile and run so you can see the words ‘Hello, World!’ on the console.

_Note: We don't really need to understand this right now. You will have questions like ‘why does it say main?’ and ‘what is that weird thing on line 1?’_

Right now, just accept it. This is how we make a simple C program run.

## Step 1: Variables - How do you store values that change?

 

\[code language="C"\]

#include &lt;stdio.h&gt;

int main() { int highScore = 5000; printf("You got the high score of %d", highScore); return 0; }

\[/code\]

This should be similar to the previous output, except it should say ‘You got the high score of 5000’.

Run this program once as written above, then change the value of 5000 in line 3 to some other whole number of your choice. Run it again. See what a variable does?

highScore is the name of a variable that can be used to store whole numbers (called integers). We know this because it says the word ‘int’ in front of it - saying store integers, under the name ‘highScore’

The printf statement has two changes to before. First, that ‘%d’ which means convert the variable to text assuming it holds integers. And after the comma, we tell it which one to convert: our variable highScore.

 

## Step 2: Conditionals - How do you make a decision?

\[code language="C"\]

#include &lt;stdio.h&gt;

int main() { int highScore = 5000; printf("You got the high score of %d", highScore);

if ( highScore &gt; 10000 ) { printf ("Wow, that's really high. Nice job"); }

return 0; }

\[/code\]

Programs need to make decisions based on variable values, just like humans do. So we change our program to give you an extra message, if it decides you have got a really good high score.

Run this program twice. First time as written. Check only one line is output, as before. Now change the highScore value in line 3 to something above 10000. Run it again. See how if statements can make decisions?

## Step 3: Loops - How do you do things repeatedly?

\[code language="C"\]

#include &lt;stdio.h&gt; int main() {

int howManyTimes = 10 ;

for( int countSoFar=0; countSoFar &lt; howManyTimes; countSoFar++ ){ printf ("This is time number %d", countSoFar); }

return 0; }

\[/code\]

Combining everything we just learned, here is a way to make programs do things more than once.

Run this as written, and you should see ten lines of output ‘This is time number 1’, ‘This is time number 2’ and so on.

Change the value of howManyTimes to some other value. Run it again. Does the output change? How?

## That’s the three basics of any programming language

In fact, for many years, that’s all computing was. Just those three things: variables, conditionals, loops.

And whilst newer languages have more ideas in them - in fact C language itself has more to it - those three basics will serve you well as a jump start.
