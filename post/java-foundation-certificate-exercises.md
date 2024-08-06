---
title: "Java Foundation Certificate Exercises"
date: "2017-03-09"
categories: 
  - "java"
---

If you are studying for the Oracle Java Foundation Certificate, you'll know that you need to understand the basic ideas in core Java.

Check your understanding by trying the exercises below.

 

## Do you understand the basics?

The topics you need to know are outlined [here](https://academy.oracle.com/pages/java_foundations_course.pdf)

Before you spend your money on the exam, it's good to check you've got that syllabus covered.

The best way to do that is by writing some short programs that cover each idea. Make sure you can do each of the exercises below.

These are basic drills to make sure you understand the ideas. They are not meant to teach the ideas; but they are the least code you can write to check your understanding.

The section headings match up to the ones in the syllabus, just to make it easy to follow.

## The Test Program

We will use a test program for every exercise, to stop us writing code that only exists to run our exercise answers.

Copy and paste the following Java code into your IDE or editor. Make sure you can run it. When it works, you will see 'Hello World' on the console.

Don't worry if you don't understand it fully - it's not what the foundations exam is about. But it will let us type our answers in easily.

\[code language="java"\]

public class JavaFoundations {

public static void main(String\[\] commandLineArguments){

new JavaFoundations().runExercise();

}

private void print( Object writeToConsole ){

System.out.println( writeToConsole.toString() );

}

private void runExercise() {

// START - Delete these lines and write your answer in here

print( "Hello World" );

// END - Delete these lines and write your answer in here

} };

\[/code\]

For each of the exercises:

- delete the contents of 'runExercise()' - you'll see the // START and // END comments to help you
- type the Java code of your answer in there

## Worked Example: How to enter your answers

Let's check we understand 'delete the lines and put out code in the runExercise() method, before we start.

Let's say we have the example question:

Q1. Write code to display "Hello, Java Foundations Ninja!"

You should

- Delete the code between the two // START and // END comments
- You should type your answer in that space
- After you have typed your code, the runExercise() method should look like this:

\[code language="java"\] private void runExercise() { // START - Delete these lines and write your answer in here print( "Hello Java Foundations Ninja!" ); // END - Delete these lines and write your answer in here } \[/code\]

As you can see, you delete the existing line of Java code, and replaced it with your own. All the exercises follow that.

## Java Data Types

Q1. Set a variable named 'topScore' to the integer value 26, and print it. Use type 'int'

Q2. Write code to set a variable named 'greetingText' to the value "Hi there", and print it. Use type 'String'

Q3. Set a variable named 'topScore' to the integer value 26. Convert this value to a String variable named 'topScoreText' and print it

## Java Methods and Library Classes

Q4. Set a String variable called 'sourceText' to "Hello World". Set an int variable called 'numberOfCharacters' to the length of the text held in sourceText.

Use the method on the String class that returns the length of that String. Print out numberOfCharacters.

Check it shows 11

Q5. Set a String variable named 'sourceText' to "these were small letters".

Set another String variable called 'upperCaseSourceText' so that it converts the text in sourceText to upper case, and print it out.

Check it shows THESE WERE SMALL LETTERS (Hint: converting to upper case - use a method found on the String class)

Q6. Create an object of the Random class, and assign it to a variable named 'randomNumbers'.

Set an int variable called 'pickedAtRandom' to the next random number and print it.

Hints:

- keyword 'new' creates objects of a class
- the variable 'randomNumbers' needs to of a type to store an object of the Random class
- What method on Random will fetch the next int?

Q7. Set an int variable called 'biggestNumber' to the larger of the two numbers 6 and 7.

Both of these numbers must appear in your code.

You must let the code decide which is the larger of the two using a method from the Math class.

Hint: the Math class does not create objects, so you won't need 'new'. But what is the right syntax to call the method you will use, if it is not on an object?

## Decision Statements

Q8. "Guess my number game":

Set an int variable named 'numberToGuess' to the value 4.

Set an int variable named 'myGuess' to 3.

Using the 'if' and 'else' keywords, write code which will

- Print out "Correct" if myGuess is the same as numberToGuess
- Print "Try Again" if it is not.

Run the code and check the output is "Try Again".

BEFORE DELETING THE CODE - change myGuess to value 4, and run again. Check it says 'Correct'

Q9. "Guess my number with switch":

Set an int variable named 'myGuess' to the number 3.

Using a switch statement, make the code print

- "Correct" when myGuess has the value of 4
- "Nearly" when myGuess has either of the values 3 or 5
- "Try Again" for every other value.

Run the code four times to check the output when you have made myGuess equal 4, myGuess equal to 9 and myGuess equal to 3 and myGuess equal to 5

## Loop Constructs

Q10. Print "Hello World" ten times, using the 'for' keyword. You must only use the "print" method once!

Q11. Print "Hello World" ten times, using the 'while' keyword. You must only use the "print" method once!

Q12. Print "Hello World" ten times, using the keywords 'do' and 'while' keyword. You must only use the "print" method once!
