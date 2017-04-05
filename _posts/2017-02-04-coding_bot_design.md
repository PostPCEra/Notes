---
layout: post
title: "Coding Bot Design"
date: 2017-02-04 16:25:06 -0700
comments: false
---

Design of a Coding Bot
=======================

## Thought process 2:
--------------

**1/ Have Test data in  YMALs Simplified Format**
 ``` 
Record1: name, age, type
ritu, 1, child
shiven, 7, child
boy2, 12, child
asr, 48, adult
padma, 44, adult
anvith, 20, adult
girlT, 19, teen
gitu, 15, teen
ishu, 13, teen
#transormations
INPUT: name, age
OUTPUT: Record1
 ``` 
Here is INPUT is subset of RECORD1, output is full Record1

**2/ arrange TEST Data Records as matrix.**
 ``` 
output = [ [ ritu , 1 ,child ],
 [ shiven, 7, child ],
 [ boy2, 12, child  ],
   ........
]

iput = [ [ ritu , 1 ],
 [ shiven, 7 ],
 [ boy2, 12 ],
   ........
]
```
**3/  Coding bot will first derermines what is the SOLUTION_TYPE**
```
  if len(input) == len(output):
    solution_type = MAP
  elif len(output) == 1
    solution_type = REDUCE
  elif len(output) < len(input):
    solution_type = FILTER

```

## Thought process 1:
----------------

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


