---
layout: post
title: "Array Change"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-03-15T15:39:55-04:00
modified: 2022-03-15T15:39:55-04:00
---

Array Change
<br><br>

You are given an array of integers. On each move you are allowed to increase exactly one of its element by one. Find the minimal number of moves required to obtain a strictly increasing sequence from the input.


**Example**<br>
For inputArray = [1, 1, 1], the output should be
arrayChange(inputArray) = 3.




~~~
function arrayChange(inputArray: number[]): number {
  let count = 0;

  for (let i = 0; i < inputArray.length; i++) {
    if (inputArray[i] >= inputArray[i + 1]) {
      const difference = (inputArray[i] + 1) - inputArray[i + 1]
      inputArray[i + 1] = inputArray[i] + 1;
      count += difference;
    }
 }

  return count;
}

 console.log(arrayChange([1, 1, 1])); => 3

~~~



We create function called arrayChange with parameter *inputArray* and local variable **count = 0** 
<br><br>
We loop the array given into the parameter *inputArray* with for loop then checks if *inputArray[i]* >= *inputArray[i + 1] 
<br><br>
If true we create variable **difference** = (inputArray[i] + 1) - inputArray[i + 1] then we switch   <br>
inputArray[i + 1] is inputArray[i] + 1 and we increase **count += difference**
<br><br>
In the end we **return count**
<br><br>
