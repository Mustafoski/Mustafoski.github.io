---
layout: post
title: "Array Conversion"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-03-16T15:39:55-04:00
modified: 2022-03-16T15:39:55-04:00
---

Array Conversion
<br><br>

Given an array of 2k integers (for some integer k), perform the following operations until the array contains only one element:

-   On the 1st, 3rd, 5th, etc. iterations (1-based) replace each pair of consecutive elements with their sum;
-   On the 2nd, 4th, 6th, etc. iterations replace each pair of consecutive elements with their product.
After the algorithm has finished, there will be a single element left in the array. Return that element.

**Example**<br>
For inputArray = [1, 2, 3, 4, 5, 6, 7, 8], the output should be
arrayConversion(inputArray) = 186.




~~~
function arrayConversion(inputArray) {
  let isOdd = true

  while (inputArray.length !== 1) {
    inputArray = someProduct(inputArray, isOdd)
    isOdd = !isOdd
  }

  return inputArray[0]
}

function someProduct(nums, isOdd) {
  const sumProducs = []
  if (isOdd) {
    for (let i = 0; i < nums.length; i += 2) {
      sumProducs.push(nums[i] + nums[i + 1])
    }
  } else {
    for (let i = 0; i < nums.length; i += 2) {
      sumProducs.push(nums[i] * nums[i + 1])
    }
  }
  return sumProducs
}
console.log(arrayConversion([1, 2, 3, 4, 5, 6, 7, 8])) => 186

~~~



We create function called arrayConversion with parameter *inputArray* and local variable **isOdd = true** 
<br><br>
We loop the array given into the parameter *inputArray* with while loop then checks if *inputArray.length* is diferent than 1. If it is we give *inputArray* = **someProduct(inputArray, isOdd)** and toggle **isOdd = !isOdd** and in the end we **return inputArray[0]**
<br><br>
We create a helper function someProduct that takes an array parameter *nums* and boolean *isOdd* also we create a local variable **sumProducs = []** <br>
<br><br>
We check if isOdd and if it is we loop with for loop where we start at 0 goes input i is less than *nums.lenght* and we increase i by 2 in every iteration.<br>
So as the description says if it is odd we use **sumProducs.push(nums[i] + nums[i + 1])**
<br><br>
Else if is even number we do the same we loop  with for loop where we start at 0 goes input i is less than *nums.lenght* and we increase i by 2 in every iteration.<br>
So as in the description says if it is even we use **sumProducs.push(nums[i] * nums[i + 1])
<br><br>
In the end we **return sumProducs**
