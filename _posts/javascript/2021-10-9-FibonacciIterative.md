---
layout: post
title: "Fibonacci Iterative"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-10-09T15:39:55-04:00
modified: 2021-10-09T15:39:55-04:00
---

## Fibonacci Iterative

Print out the n-th entry in the fibonacci series.
The fibonacci series is an ordering of numbers where each number is the sum of the preceeding two.

Example:<br>
fibonacciIterative(8) 21  <br>




~~~

function fibonacciIterative(n) {
  let arr = [0,1]
  for(let i = 2; i < n + 1; i++) {
    arr.push(arr[i-2]+ arr[i-1])
  }

  return arr[n]
}
fibonacciIterative(8) 21
~~~
___

We create a function fibonacciIterative with parameter of number *n* and variable *arr*=[0,1]
<br><br>
We loop with for loop starting from 2 since we have the first two numbers in the result array, we iterate until is less or equal to *n* and *i*++
<br><br>
We use variable array *arr* and do ***arr.push(arr[i-2] + arr[i-1])*** 
<br><br>
push method adds item in the array and inside this push we have last number from the for loop and the one before that added
<br><br>
In the end we return ***return arr[n]***

