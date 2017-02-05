---
layout: post
title: "Coding Bot Design"
date: 2017-02-04 16:25:06 -0700
comments: false
---

Design of a Coding Bot
=======================

### ingradients:
+ unit test suite JSON file, from it generate unit test program
+ have a list of INPUT to OUTPUT Mapping functions
+ read 'test case file' and figure out which mapping it belongs and geneate code 

### maping samples:  
+ List(N) -> List(M)  -- (Map ) compute squares of List of numbers
+ List(N) -> n   -- (N to 1) find largest or smallest number of a given List of numbers 
+ List(N) -> List(N1) -- (Filter) extract odd numbers in a List, extract prime numbers in a List

### unit test suite JSON file:
- convert the following JSON into a 'Pytest' program code  ( Nose 2 and unittest seems bit old )  
- the program does will try to find relation ( is is sqrt , x^2 , 2x-1  whatever ) 
```
{
 problem_type : "map",  // you specify one of "map" , "reduce" or "filter"
 test_suite : [
    {
     case_desc : "positive numbers" ,
     input : [ 1,5,9,15, 2, 50, 6 ],
     output : [1, 25, 81, 225, 4, 2500, 12 ] ,
     },
    {
     case_desc : "mixed numbers" ,
     input : [ 1,5,-9,25, 2, 5, -4 ],
     output : [1, 25, 81, 225, 4, 25, 16 ] ,
     },
 ]
 
 }
```
- This can be done with Class Objects ( List of Person objects), or JSON files of Objects ( a JSON file with List of People data )


### some Markdown samples below

```
$ git remote add upstream git@github.com:scotte/jekyll-clean.git
```

```python
import random

# Roll the die
roll = random.randint(1, 20)
print('You rolled a %d.' % roll)
```
