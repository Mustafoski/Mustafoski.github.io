---
layout: post
title: "Fibonacci Iterative v2"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-01-25T15:39:55-04:00
modified: 2022-01-25T15:39:55-04:00
---

## Fibonacci Iterative v2

Print out the n-th entry in the fibonacci series.
The fibonacci series is an ordering of numbers where each number is the sum of the preceeding two.

Example:<br>
fibonacciIterative(8) 21  <br>




~~~

function fib(n) {
  const result = [0, 1];
  for (let i = 2; i <= n; i++) {
    const a = result[i - 1];
    const b = result[i - 2];
    result.push(a + b);
  }
  return result[n];
}
fibonacciIterative(8) 21
~~~
___

We create a function fib with parameter of *n* and we create a variable *result*=[0,1]
<br><br>
We loop with for loop starting from 2 since we have the first two numbers in the result array, we iterate until is less or equal to *n* and *i*++
<br><br>
We create two variables a and b ***a = result[i - 1] and b = result[i - 2]***
<br><br>
Variable *a* is last number from the loop since we substract - 1 and *b* is the number before *a* then we ***result.push(a + b)*** We use JavaScript push method to push the result of *a*+*b*
<br><br>
In the end we return ***return result[n]***



In the end we return answer

