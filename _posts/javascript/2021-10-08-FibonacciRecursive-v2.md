---
layout: post
title: "fibonacci Recursive v2"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-10-10T15:39:55-04:00
modified: 2021-10-10T15:39:55-04:00
---

## Fibonacci  Recursive v2

Finding wether if algorithm can works recorsevily

Example:<br>
findFactorialRecurative(5)} 24  <br>




~~~

function fib(n) {
  if (n < 2) {
    return n;
  }
  return fib(n-1) + fib (n-2);
}
fib(8) 21

~~~
___

We create a function fib with parameter of *n* 
<br><br>

We check wheter number is less than 2 and if it is we assing answer to n.<br>

We return fibonacciIterativeRecursive(n-1) + fibonacciIterativeRecursive (n-1) <br>

In the end we return answer

