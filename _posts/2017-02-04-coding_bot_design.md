---
layout: post
title: "Coding Bot Design"
date: 2017-02-04 16:25:06 -0700
comments: false
---

Real-time Assisted Programming (RAP ) : Design of a Coding Bot 
=======================

+ 0/ Cost per line of CODE : $1 per line
  + $1 /LOC : Having a base line pay say $1 per each line of code that pushed to production. Blnak lines, block markers { } , import , varriable declarations DOES NOT count. There will be 'Automated CODE Compacter' if someone try to Bloat CODE.
  + So for a $5000 /month pay of 20 working days/month , one has to produce 250 LOC/day ( Lines of Code per day )
  + so a CODING BOT Tool, which produce 10% more that is 25 Lines of code/day is saving $6000/year (10% of $60K)
  + So Saving $6000, then $600/year Subscription cost is justed that is  10%
  
  + so using a Library like [Cleaver Formater](http://nosir.github.io/cleave.js/) , it reduces 5 lines of Code per each INPUT Filed in UI CODE, 5 Lines less Testing for QA Team.
  
+ 1/ Sourced : Build AI that does [real-time assisted programming](https://blog.sourced.tech/post/our-roadmap/)
  + Emulating the work of human developers means must have built an understanding of the different ways a piece of code can be written.
  + Let’s consider a simple piece of code written by a developer: a function that has well **defined inputs and outputs** and no side-effects, and you imagine how a machine might be able to write this.
  + If you imagine how a developer writes this same simple program, you start seeing the notion of intuition and experience. Performance is no longer the only notion that defines the right program, such others may be: simplicity, elegance, readability, extensibility, etc.
  
  + The practical application is technology that can suggest you code, rewrite your code, change your code’s style, optimize code and applications we haven’t yet thought off.

+ [2/ Kite : Topnotch Team](https://kite.com/aboutus) - they need to extend this 'simple Syntax help' to 'Coding BOT' like what i envinioised here 
+ a Site like stackOVerflow/Kite where you have Catalogue Repository of Solutions and 'Developer' pick one from  'Editor itself' 
+ developer give input, on a picked solution , it shows CODE and OUTPUT like our REAL TIME Python Editor ( no compile etc..), User can go back and front Arrow  to see Values ,and Tweak CODE ...

## Thought process 4:
--------------
How User Interface Works
+ user picks from a SEARCH Box, he wanted solution for 'Text processing' -> extraction By Delimit . Then User is presented with INPUT & OUTPUT sample of pre-templates. User select one Template. example
  + @input str = 'This is some text"," this is news for today"" today headline is US POT visits China"," EU presidnet visits Asia'
  + @param delimiters = [ '","' ,  '""' ]
  + @output lst = [ 'This is some text', 'this is news for today', 'today headline is US POT visits China', EU President visits Asia' ]
+ by looking above user can modify @input and or @param, program will show CODE, user run with mutilple case of INPUT 
+ IF your did not specify @param Delimiters, BOT can detect as follow
+ pointer = str[len(lst[0])], from this Char advance pointer till it match  with first Char of lst[1] , those many Char string is 'delimier 1' , do same fo find other delimiters 

## Thought process 3:
--------------

+ Text processing
  + string delimit ( like our Soloka delimit by \",\" )
  + string chunks ( or Chars) removal
  + extract Reg Ex data
+ Date Format convertions ( Calender )
  + convert Date/Time values from one format to another 
  
+ Sorting
  + Sort Various objects such as Lists(Array), Dictionaries ( Hash) . examples
  + sort by: name, age DESC

+ Filtering
  + Objects  ( object of (name, age, salary) )

+ Mapping

with respect to base Atomic operations MAP/Reduce/Filter
 + MAP
  + MAP_FUNC : Functional MAP , ex find Squares of a given input list [ 1,5, 4, 12 ], the output Uniform Functional relationship
  + MAP_CAT : Category MAP , FizzBuzz problem is a Category Map. you Map input to output by bucketing into certain categories 
  + [ name, age , type] with output Type being one of ( child, teen, adult) based on age,  this is MAP_CAT , here category is homogenious
  
 + How Coding Bot will figure it out MAP_FUNC vs. MAP_CAT . When ALL output Elements are of same type, then BOT make  is as MAP_FUNC
 + How the BOT go about  FizBuzz vs. Person Type problmes
  + FizzBuzz : if number is multiple of 3 print 'Fizz', if multiple of 5 , print 'Buzz', mul of both print 'FizzBuzz' , otherwise print number
  + FizzBuzz is a MAP not FILTER becoz len(output) = len(input) , FizzBuzz is a CATEGORY map, where as Squares is a Functonal map (uniform function )
 ``` 
 input = [ 1,2,3,4,5,6,7,9.10.11,12,13,14,15, 16,17]
 output = [ 1,2, 'Fizz, 4, 'Buzz', 'Fizz', 7, 8,'Fizz', 'Buzz, ..  14, 'FizzBuzz', 16, 17 ]
 
 map_func, map_cat = False  # init
 reduce = False
 filter - False
 
 if len(output) == 1:
   reduce = True
 elif len(input) < len(output):
   filter = True
 elif len(input) == len(output):
    inp_type = [ type(x) for x in output ]

    if ( len( set(inp_type) )  == 1 ):
        map_func = True
    else
        map_cat = True
         
 if (map_cat) :
   out_dict = { }
   i = 0
   lenght = len(output)
   while ( i < length):
     build out_dict
     
  out_dict = {  1: [1], 2: [2], 'Fizz' : [ 3, 6, 9, 12,  18] , 'buzz' : [5, 10, 20 ],  'fizzbuzz': [15,30,45], 4: [4] .. 11:[11] ] 
  
  relations = [ ]
  for i, v in out_dict:
     rel = find_relation(v)
     realtions.add(rel)
     
  relations = [ n2n, n2n, [ multiple3, 'Fizz' ] , [ multiple5, 'buzz' ] , [multiple15, 'fizzbuzz ], n2n, n2n ]
  # now BOT will write CODE file based on above 'relations' list
  
  for x in lst:
    if multiple15(x):
       out.append('FizzBuzz')
    elif multiple3(x):
       out.append('Fizz')
    elif multiple5(x):
      out.append('Buzz')
    else:
      out.append(x)
  
 ``` 
## Thought process 2:
--------------

Application in real life:
 + IF NOT complete BOT coding, you can have a 'GUIDED BOT', meaning you give INPUT and OUTPUT data for Each INTERMDIATE Step, then BOT produce Code, you may modify it bit as needed.
 + Advantage with this is , your CODE is UNIT tested as YOU Write 
 + Having Data in hand before CODING, will improve your Logic/Algorithamic Thinking and may provide 25% more CODE in a given TIME


**1/ Have Test data in  YMALs Simplified Format**
 ```  
DEFINE Record1(name, age, type)  # makesure you provide DATA for EDGE cases, start data with MIN value and End with MAX value
DATA Record1
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
INPUT Record1(name, age)
OUTPUT Record1
OUTPUT(type) = F(INPUT(age)) # optinoally you can sepcify relationship, to make BOT life easy
END
``` 
Here is Reserved words DEFINE DATA INPUT OUTPUT will help form SYNTAX Rules, so a program can process this then construct and spit Code as output

Here INPUT is subset of Record1, output is full Record1. This kid of format Eliminate the need to Repeat of Data for INPUT and OUTPUT two times.

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
     [ [ child , [1, 7, 12 ] ,  { min:1  , max:12  } ], 
       [ adult , [20, 44, 48 ] ,  { min:20  , max:48  } ], 
       [ teen ,  [13,15,16,19 ] ,  { min:13 , max:19  } ]
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


