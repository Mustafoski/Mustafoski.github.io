---
layout: post
title: "FibonacciIterative"
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

## FibonacciIterative

Finding wether if algorithm can works recorsevily

Example:<br>
fibonacciIterative(8)} 21  <br>




~~~

function fibonacciIterative(n) {
  if (n < 2) {
    return n;
  }
  return fibonacciIterative(n-1) + fibonacciIterative (n-2);
}
fibonacciIterative(8) 21

~~~
___

We create a function fibonacciIterative with parameter of number <br>

We check wheter number is less than 2 and if it is we assing answer to n.<br>

We return fibonacciIterative(n-1) + fibonacciIterative (n-2) <br>

In the end we return answer

