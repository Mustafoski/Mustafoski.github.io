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
date: 2022-01-26T15:39:55-04:00
modified: 2022-01-26T15:39:55-04:00
---

## Fibonacci  Recursive v2

Print out the n-th entry in the fibonacci series.
The fibonacci series is an ordering of numbers where each number is the sum of the preceeding two.

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
We check wheter *n* is less than 2 and if it is we return to n.
<br><br>
In the end we return fib(n-1) + fib (n-1) <br>



