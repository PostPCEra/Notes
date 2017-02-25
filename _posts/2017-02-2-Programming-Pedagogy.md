---
layout: post
title: "Programming-Pedagogy"
date: 2017-02-24 15:25:06 -0800
comments: false
---

#### Pedagody (noun)

> the method and practice of teaching, especially as an academic subject or theoretical concept.

## Programming Pedagogy
+ I. Basic Concepts of any Programming Language
+ II. Fundamental Concepts of Progamming ( building blocks )
+ III. Content & Tutorials


### I. Basic Concepts of any Programming Language 
+ Variables
+ Control flow
  + Selection ( Branching), Iteration (Looping)
    + It is calling Branching coz, it is Branching of a Tree ( or How you Control the Flow )
    + never start with FOR loop, they get spoiled , always do couple of sessions with WHILE only
+ Syntax
+ Functions
+ Data Structures 

> [Note 1](https://howtoprogramwithjava.com/programming-101-the-5-basic-concepts-of-any-programming-language/){:target="_blank"} - Tools as said here may not be part of BASIC Concepts

> [Python here](https://www.programiz.com/python-programming){:target="_blank"} -  File Handing, Objects & Classes may come under PART 2 of Programming Language, while above Part 1 is BASICS

> [Control statements gif](http://edusagar.com/assets/img/control-flow.gif){:target="_blank"}


###  II. Fundamental Concepts of Progamming ( building blocks )
1. **First-order functions** ( Atomic functions )
 + Map, Reduce , Filter 
 + SUM, MIN, MAX ( finding sum of a LIST, finding Largest element in a List )
2. **Modeliing**
 + In programming nobody gives a problem like there is a List find largest Value,  they give a problem such as
  + A new shop near you is selling n paintings.You have k < n friends and you wouldlike to buy each of your friends a painting from the shop. Return the minimal amountof money you will need to spend.
  + you need to comeup with a STRUCTURE to mimic (Model) the Problem , this process is called Modelling.
3. **De-compostion** ( what is compose? like in Compose a Story: take multiple parts and combine them into ONE )
 + braking problem in to atomic Units and connect them
 +
4. **Modelling Complex example:**
 + You are the first person standing in a line for a Concert Tickets. You bought 2 tickets and your friend just called he won't be able to join you for the concert. Now you have one extra ticket to sell to somebody ( there are 100s of people in line), you thought for a  second and decided you will sell that ticket to a person who is wearing same colour shirt (top) as yours starting from LAST person of the Line.
 + write a function to calculate the Distance (how many people are in) between both of you 
 + Concert Manager came to know your creative way of giving ticket and impressed with your method. To appreciate you, manager announced he follows the same method as yours, but gives two tickets FREE to the Fartherest apart two people wearing same color shirt (top) in the line. Write a program to find that distance ( bonus : find those 2 lucky people, say person 5 and person 86 etc.. ) 

### III. Content & Tutorials : [Good Explanation here](https://howtoprogramwithjava.com/programming-101-the-5-basic-concepts-of-any-programming-language/){:target="_blank"}
+ **1. Variables**
 + any name   a, first, lastname, toyname , ...
 + variable store value :  numbers , strings,  Boolean 
 + Boolean : show Visually step by how it changes values : oddday = True ,  oddday = not(oddday)  
 + **experssion** :  1 + 5 , 6 - 2 , 43 * 5 , 20 / 5 ,  a + 5 ,  b - 2
    + Math expression: Numbers, symbols and operators (such as + and ×) grouped together that show the value of something. [2×3 , x + 7 are expressions]( http://www.mathsisfun.com/definitions/expression.html){:target="_blank"}
 
+ **2. IF startments**
 + ( should we take user input at this time? to make it interesting to the user )
 + give good example , like temparate input and print a statement
 
+ **3. Iteration ( Looping )**
 + problem 1: Say you have $100 in bank you are withdrawing $25 each day, show the probgram to show each Withdraw
 + problem 2: show balance and Withdraw each day
 + problem 3 : you have $100 in bank, withdraw $30 each day
 + 
 + problme 4: $200 balance, withdraw $30 each day.  show Day number , withdraw amount, balance 
 + problme 5: $500 balance, withdraw day 1 $20, day 2 $30, day 3 $20, day 4 $30 .. you repeat this pattern till you are allowed to Withdraw 
 
``` 
       if oddday:
          amt = 20
        else:
          amt = 30
          
        oddday = not (oddday) # keep blank lines you know the logical grouping , easy on your Brain , said so Python PEP20
```

### First-order functions
+ Sum
+ Max
+ Min

### Higher-order functions
+ Map

-------------------------------
### Patterns
+ **Accumulation**
+ **Keep One**
+ **Filter ( Keep Some )**
+ **Driver function and Core function**
+ **At higher level, many porgramming tasks are one of **  a) Map  b) Reduce or c) Filter

+ **Accumulation**
  - Accumulation into  either a variable ( calculate Sum of a List numbers )  or in a List ( append to List in each iteration )
  
```
def find_sum(lst):
  sum = 0
  for x in lst:
     sum = sum + x
   return sum
    
    
 def find_squares(lst):
 sq_lst = []
 for x in lst:
     sq_lst.append( x * x )   
 return sq_lst          
 ```

+ **Keep One**
  - ex. find the largest number in a List
  
```
def find_large(lst):
  large = lst[0]
  for x in lst:
     if x > large:
        large = x 
  return large
 ```

+ **Filter ( Keep Some )**
  - return a List whose elements are greater than avarge of List numbers.
  - this is ACCUMULATION,  Formula , Filter as last steps

+ **Driver function and Core function**
  - Driver function = [House keeping](https://en.wikipedia.org/wiki/Housekeeping_(computing) ) + Feeder 
  - Driver do the house keeping , a) chunk out appropriate INPUT to send to CORE b) do call Core Function and perform 'Accumulation or Keep ONE ' operation 
  
+ The **mainline logic, in every computer program**,[can follow a general structure](http://cdalight.blogspot.com/2005/02/understanding-mainline-logical-flow.html). These steps are **housekeeping, the main loop, and the end-of-job-routine**. 
  
### Housekeeping could include (but is not limited to) the following activities:
  - aving and restoring program state for called functions (including general purpose registers and return address)
  - Obtaining local memory on the stack
  - **Initializing local variables** at the start of a program or function
  - Freeing local memory on the stack on exit from a function
  - Garbage collection
  - **data conversion** ( as we did in max_span() Pytest program )
  
------------------------
### Teach Yourself Programming in Ten Years - Peter Norvig (google)
Pter Norvig quoting the following from the book [Cognition in Practice:](https://www.amazon.com/exec/obidos/ASIN/0521357349)

+ **the most effective learning requires** 
  - a well-defined task with an appropriate difficulty level for the particular individual, 
  - informative feedback, and 
  - opportunities for repetition and corrections of errors.



### Programmer Competency Matrix
+ [author sates Level 0/1 to 3](http://sijinjoseph.com/programmer-competency-matrix/)
  -  we (asr) may form a similar Levels for  Learners such as
  - Level 0 :
  - Level 1 : can understand variables, IF statements ,  loops such as FOR .  But can not Debug a problem in the code
  - Level 2 : can debug code, but can not decompose the problem, can not identify Patterns , can not Apply patterns
  - Level 3 : can Identify patterns, can learn from error correction feedback

### What's the difference between Entry [Level/Jr/Sr developers?](http://softwareengineering.stackexchange.com/questions/14914/whats-the-difference-between-entry-level-jr-sr-developers) 

I would say entry level and Junior are the same thing. 

  - They are just out of school and have less than two years of work experience. 
  - They are assigned the least complex tasks and should be supervised fairly closely. 
  - Generally they know about 10% of what they think they know. 
  - Usually they have not been through the whole development cycle and so often make **some very naive choices** if given the opportunity to choose. 
  - Sadly many of them don't actually care what the requirement is, they **want to build things their way**. 
  - They often have **poor debugging skills.**
  
  - [another Stack answer](http://softwareengineering.stackexchange.com/questions/136163/whats-the-difference-between-junior-middle-and-senior-developers)
  - A Junior developer will need near-constant help. 
  - Not only will they not know the business domain, but they may also struggle with the **fundamentals of the language or the toolset**.
   - They don't know what they don't know, so without guidance, they will **make frequent mistakes** which, if not kept on top of, **will derail the wider team.**
