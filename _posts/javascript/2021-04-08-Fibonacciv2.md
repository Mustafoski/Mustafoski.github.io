---
layout: post
title: "Fibonacci-v2"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-08-04T15:39:55-04:00
modified: 2019-08-04T15:39:55-04:00
---

## Fibonacci v2
In mathematics, the Fibonacci numbers, commonly denoted Fn, form a sequence, called the Fibonacci sequence, such that each number is the sum of the two preceding ones, starting from 0 and 1. 
___

> ##For Example
[
  1,  2,  3, 5,
  8, 13, 21
]
Should return true<br>
##
<br>

___


~~~
function generateFibonacci(howMany) {
  let x = 1;
  let y = 1;
  let sequence = [x, y];
  Array(howMany)
    .fill()
    .forEach(() => {
      let sum = x + y;
      sequence.push(sum);
      x = y;
      y = sum;
    });
  return sequence;
}

console.log(generateFibonacci(5));

~~~

___

We create a function generateFibonacci with parameter howmMany, we know that fibonacci sequence starts with 1 and 1 so we start creating x to 1 and y to 1 and we initiate the sequence array to 1,1. 
<br><br>
Then we create foreach function that starts with Array build in function and we fill it with the sum of x and y and we push that sum into the sequence array then we assign x = y and y = sum 
<br><br>
In the end we return the sequnce array