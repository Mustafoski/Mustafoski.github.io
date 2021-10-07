---
layout: post
title: "fibonacciIterativeRecursive"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-11-18T15:39:55-04:00
modified: 2021-11-18T15:39:55-04:00
---

## fibonacciIterativeRecursive

Finding wether if algorithm can works recorsevily

Example:<br>
findFactorialRecurative(5)} 24  <br>




~~~

function fibonacciIterativeRecursive(n) {
  if (n < 2) {
    return n;
  }
  return fibonacciIterativeRecursive(n-1) + fibonacciIterativeRecursive (n-2);
}
fibonacciIterativeRecursive(8) 21

~~~
___

We create a function fibonacciIterativeRecursive with parameter of number <br>

We check wheter number is less than 2 and if it is we assing answer to n.<br>

We return fibonacciIterativeRecursive(n-1) + fibonacciIterativeRecursive (n-1) <br>

In the end we return answer

