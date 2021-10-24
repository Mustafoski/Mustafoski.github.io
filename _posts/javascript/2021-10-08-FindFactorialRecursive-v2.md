---
layout: post
title: "Find Factorial Recursive"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-10-10T15:39:55-04:00
modified: 2021-10-18T15:39:55-04:00
---

## Find Factorial Recursive

Finding wether if algorithm can works recorsevily

Example:<br>
findFactorialRecurative(5)}  120 <br>




~~~

function findFactorialRecursive(number) {
  if ( number == 2){
    return 2;
  }
  return number * findFactorialRecursive(number-1);
}

findFactorialRecursive(5)

~~~

We create a function findFactorialRecurative with parameter of number <br>

We check wheter number is equal to 2 and if it is we return  2.<br>

We return the number *  findFactorialRecurative(number-1) <br>

So we have number 5 * 4 * 3* 2 * 1 = 120

