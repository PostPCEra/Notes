---
layout: post
title: "PyTest sample for Gitu program"
date: 2017-02-06 15:25:06 -0800
comments: false
---

## PyTest sample for Gitu program
PyTest parameter passing takes only Strings and Numbers, so passed LIST as String and re-constructed as LIST and passed to driver()

[Parametrizing fixtures and test functions](http://doc.pytest.org/en/latest/parametrize.html)

### Pytest code
```
from max_span import driver

import pytest

@pytest.mark.parametrize("test_input,expected,desc", [
        ( '[ 4]'  , 1, "1: Just one element"),
        ( '[4, 2]' , 1, "2: two distinct elements "),
        ( '[4, 4]' , 2, "3: two dup elements"),
        ( '[4, 3, 4]' , 3, "4: three elements"),
        ( '[ 4, 5, 1, 3, 8,8,2,6]' , 2, "5: two elements 8,8"),
        ( '[ 4, 5, 1, 3, 4,8,7,6]' , 5, "6: five elements 4..4"),
        ( '[ 4, 5, 1, 3, 4,8,5,6]' , 6, "7: six elements 5..5 over taking span 5 of 4..4"),
])

def test_eval(test_input, expected, desc):
      # PyTest parameter passing takes only Strings and Numbers, 
       # so passed LIST as String and re-constructed as LIST and passed to driver()

        lst = [int(x) for x in test_input[1:-1].split(',') ]
        assert driver(lst) == expected , desc


```

### main program code
```
def max_span(lis):
    l = len(lis)
    while (l > 0):
        l = l - 1
        if (lis[0] == lis[l]):
            return l + 1
        
def driver(lis):
    max1 = 0
    for x in xrange(0,len(lis)-1): 
        m2 = max_span(lis[x:])
        if m2 > max1: 
            max1 = m2
    return max1

# main call 
if __name__ == "__main__": 
    lis = [ 4, 5, 6, 3, 4,4,5,6]
    mlen = driver(lis)
    print(mlen)

# Testing : run this command from Terminal
# pytest -v test_max_span.py
```
