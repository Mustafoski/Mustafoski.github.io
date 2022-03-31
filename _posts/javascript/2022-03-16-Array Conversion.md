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
We loop the array given into the parameter *inputArray* with for loop then checks if *inputArray[i]* >= *inputArray[i + 1] 
<br><br>
If true we create variable **difference** = (inputArray[i] + 1) - inputArray[i + 1] then we switch   <br>
inputArray[i + 1] is inputArray[i] + 1 and we increase **count += difference**
<br><br>
In the end we **return count**
<br><br>
