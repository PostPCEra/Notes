---
layout: post
title: "Coding Bot Design"
date: 2017-02-04 16:25:06 -0700
comments: false
---

Design of a Coding Bot
=======================

### ingradients:
+ unit test case JSON file, from it generate unit test program
+ have a list of INPUT to OUTPUT Mapping functions
+ read 'test case file' and figure out which mapping it belongs and geneate code 

### maping samples:  
+ List(N) -> List(M)  -- (Map ) compute squares of List of numbers
+ List(N) -> n   -- (N to 1) find largest or smallest number of a given List of numbers 
+ List(N) -> List(N1) -- (Filter) extract odd numbers in a List, extract prime numbers in a List


```
$ git remote add upstream git@github.com:scotte/jekyll-clean.git
```

```python
import random

# Roll the die
roll = random.randint(1, 20)
print('You rolled a %d.' % roll)
```
