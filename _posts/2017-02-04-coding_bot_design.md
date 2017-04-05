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
Record1: name, age, type  # makesure you provide DATA for EDGE cases, good practice start data with MIN value and End with MAX value
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
OUTPUT(type) = F(input(age)) # optinoally you can sepcify relationship, to make BOT life easy
 ``` 
Here is INPUT is subset of RECORD1, output is full Record1

**2/ BOT will arrange TEST Data Records as matrix.**
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

  if ( solution_type == MAP ): 
      dim_input , dim_output = 0
    
      dim_input = dim(input) # function returns TUPLE such as ( 5, 2)  indicatiing theere are 5 rows and 2 Columns
      dim_output = dim(out)  # ( 5, 3 )  3 Columns
      
      if (dim_input[0] == 1 and dim_output[0] == 1 ):
           s_type2 = MAP_SIMPLE_LINEAR   # example: from input [ 1,3, 5] calculate squares of input as [ 1, 9, 25 ]
      else:
           s_type2 = MAP_OBJECT   # Object like above people age, type MAP
        
```
**4/ fining the Input, output relation function

```
  based on Spec line OUTPUT(type) = F(input(age)), Bot will arrange matrix as
     [ [ child , [  ] ,  { min:  , max:  } ], 
       [ adult , [  ] ,  { min:  , max:  } ], 
       [ teen ,  [  ] ,  { min:  , max:  } ]
     ]
     based on the above matrix it will write the CODE ...
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


