# Hello Turtles! A quick intro to Python

```python
while alive:
    eat
    sleep
    code
```

> Unfortunately no one can be told what coding is like. You have to experience it for yourself. This is your last chance. After this, there is no turning back. You take the blue pill—the story ends, you wake up in a normal classroom and believe whatever you want to believe. You take the red pill—you stay in Wonderland, and I show you how deep the rabbit hole goes. You say goodbye to your family and friends, regular sleep, fresh air, daylight, and a balanced diet.

> Remember, all I'm offering is the truth. Nothing more...

> Follow me...

<!---![red_blue_pill](assets/red-pill-blue-pill.jpg width=250)--->
<img src="assets/red-pill-blue-pill.jpg" width="100" height="100"/>


## Background stuff

Most people think that computers are incredibly smart. Actually they are seriously dumb. In fact, all they know how to do is add up 1's and 0's, and even then they reckon that `1 + 1 = 10`.

What makes them seem so smart is that they are able to add 1's and 0's really quickly. Mindboggling quickly! Millions of times per second! And this lets them use the simple task of adding to produce astonishing outputs. Rather like the way you can produce a complex image just by adding black dots to a white page.

The job of the computer programmer is to tell the computer how to add the 1's and 0's to make the complex 'picture'. To do this we write code in a programming language. There are many programming languages: Java, C++, Prolog, and Swift and we will look at some of them later, but for now we will be using Python. It is a free, open-source, object-orientated language that closely resembles the English language which makes it a great language to learn for beginners as well as seasoned professionals.

But don't let anyone convince you that just because python is easy to learn it is a beginners' language. It is used by scientists and IT professionals everywhere. Organisations that use Python include Instagram, YouTube, Reddit, NASA, and Usersnap (who wrote about their Python experience [here](http://usersnap.com/blog/cloud-based-saas-architecture-fundamentals/)).

As well as being dumb, computers are also frustratingly obedient. Just like the [cyborg Hymie in Get Smart](/assets/Get_Smart_-_Hymie_classic_reaction.mp4) they do exactly what you tell them to do, not what you meant to tell them to do. This is the bane of a programmers life - errors in your code that you need to find and fix. To be a good coder you need to learn to think like a computer and that means logically and one step at a time.

## Your mission, should you choose to accept it

We are going to drop you in the deep end (well the shallow bit of the deep end) and get you coding straight away. 

Have a look at the code on the in the main.py file. See if you can work out what it does and answer the questions below? Be brave and press the run button to execute the code. Did it do what you predicted?

## Let's break it down.

 Lines 1 to 5:

```
""" Simple script introducing python using turtle.

A script to introduce python 3.x to Year 11 SDD students @ Aurora College
Introduces basic concepts using the turtle module
"""
```

This is a special type of comment called a _docstring_ which gives a simple description of what the program does. We will talk about comments in more depth as we go on but they are really important. Get into the habit of using comments as you write your code. They explain to you and others what you are doing and why. It may seem obvious to you at the time but when you come to revise your code weeks or months later you will come across stuff and ask "what on earth was I trying to do there?"

Line 2:

There is no line 2 because it is important to use white-space in a way that keeps your code readable.

Lines 7 to 13:

```
__author__ = "Dr G"
__copyright__ = "Copyright 2018, NSW Dept. Ed."
__license__ = "GPL"
__version__ = "1.0.1"
__maintainer__ = "Dr G"
__email__ = "geoff.goldrick@det.nsw.edu.au"
__status__ = "Development"
```

This is the metadata and is used to identify important information about the code. You normally wouldn't see this in an introduction to programming but I reckon good habits start early. In general you should have something that looks like lines 1 to 13 at the beginning of all of your code. Most of these fields are self evident, but for `__status__` you should use "Prototype" when you are doing the initial mucking around, "Development"  for your work in progress and "Production" for your final submission.

Line 15:

```
import turtle as t
```

The python environment has a lot of standard inbuilt functions but often we want something more, so we add functionality by importing modules. For this exercise we need to import the _turtle_ module. We will give it the shorthand name 't' so we don't have to keep writing 'turtle' all the time.

Line 17:

```
donatello = t.Turtle()
```

Creates a turtle. It might help if our first turtle was a technological genius so lets call it donatello. To use the correct geek jargon this line creates an instance of the class turtle and assigns that instance to the variable name donatello.

NOTE: Python is sensitive, case sensitive, that is. So typing `t.Turtle` is not the same as `t.turtle` and `donatello` is not the same as `Donatello.`

Line 19:

```
donatello.forward(100)
```

To state the bleedin' obvious, this line moves donatello forward 100 pixels.


## Mash it up

This isn't the most exciting code in the world but it is better than the usual introduction to programming that just teaches you to print "hello world". Let's make it even better.

First, edit the header block (lines 1 - 13) to change the author, email, status details etc.  Now let's get coding.

For a start, donatello doesn't look much like a turtle so let's fix that . Copy and paste the code below to replace line 17.

```
donatello = t.Turtle()
donatello.shape("turtle")
```

Now, this is a ninja turtle so it should be able to do something more impressive that walk in a straight line so replace the forward command with the following (the indentation is really important in python):

```
for counter in range(1,4):
  donatello.forward(100)
  donatello.left(90)
```

What do you think this code should do? Run the code, then compare your prediction with the actual result.

You probably predicted that this code would draw a square, and that would be a logical guess, but this example illustrates a little quirk of the coding world when compared with the real world. For reasons that I hope will become clear when we start playing around with bits and bytes, coders usually count starting with zero and don't include the number indicating the top of the range. So a range of 4 would be the numbers 0,1,2,3. But if we specify a different beginning to our range, by starting at 1, it doesn't affect how the number indicating the top of the range is treated and the numbers now include 1,2,3. Confused? You'll struggle with this a bit a first but then you will get used to it.

Change the code so that it makes a complete square.


### Two's company

Sometimes one turtle is not enough so so lets add another. And they wont want to be on top of each other so we will move raphael down and to the left, and ask raph to do something different. Replace the code from line 17 onwards with the code below. _**Note: we don't have to specify the bottom of a range and if we don't it is assumed to be zero.**_

```
donatello = t.Turtle()
donatello.shape("turtle")
donatello.color("purple")

raphael = t.Turtle()
raphael.shape("turtle")
raphael.color("red")
raphael.penup()
raphael.goto(-100,-50)
raphael.pendown()

for counter in range(4):
  donatello.forward(100)
  donatello.left(90)
  raphael.circle(counter*10)  
```

Run the code then describe what the following lines of code do:

```
raphael.penup()
raphael.goto(-100,-50)
raphael.pendown()
```

and

```
raphael.circle(counter*10)
```

> put your answer here
>

NOTE: Indentation is very important to python, each loop instruction affects everything that is indented below it. In other words, indentation defines the beginning and end of the loop.

NOTE: Punctuation is also important in python, as you will find to your frustration. Try running the code without the colon at the end of the _`for`_ line and see what happens. You will have to click on the console tab to see the error message.

One final little trick before I set you free. The code above shows an example of completing a repetitive task using a _for loop_. A _for loop_ is an example of a _control structure_ which are really powerful tools and feature prominently in most coding solutions. They become even more powerful when they are nested, so replace the four lines of the _for loop_ with this _nested for loop_ then run it and see what it does. _**Note: we don't have to specify the bottom of a range and if we don't it is assumed to be zero.**_

```
for counter1 in range(10):
  for counter2 in range(4):
    donatello.forward(100)
    donatello.left(90)
    raphael.circle(counter2*counter1*3)
  donatello.left(36)
  raphael.right(72)
```

# Fly little turtles

Now its your turn. Using the [cheat sheet of turtle commands](/assets/Turtle Graphics.pdf) as your guide, play around for the rest of the lesson and try and make the most beautiful turtle art you can. By beautiful we mean not just visually but in terms of your coding as well.

Submit your code before the next lesson and they will be judged by your peers and the best entry will win a gummy bear.

# Resources

* [Turtle Cheat Sheet](/assets/Turtle Graphics.pdf)
* http://www.eg.bucknell.edu/~hyde/Python3/TurtleDirections.html


