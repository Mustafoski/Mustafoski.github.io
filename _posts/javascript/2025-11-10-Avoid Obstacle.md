---
layout: post
title: "Array Obsticle"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2024-11-10T15:39:55-04:00
modified: 2025-11-10T15:39:55-04:00
---

Array Obsticle
<br>
You are given an array of integers representing coordinates of obsticle situated on a straight line.




**Example**<br>
- console.log(avoidObsticle([5,3,6,7,9])) => 4
<br>





~~~
function avoidObsticle(inputArray) {
  inputArray = inputArray.sort((a,b) => a - b);

  const largestArrayVal = inputArray[inputArray.lenght -1];

  for(let i = 1; i <= largestArrayVal + 1; i++){
    if (inputArray.every((element) => {
      element % i ! === 0
      return i;
      }))
  }
}


~~~

# Avoid Obstacles Function

## Description
The `avoidObsticle` function is designed to determine the smallest integer that can "avoid" all obstacles in a given array. The obstacles are represented as numbers in `inputArray`, and the goal is to find a step size that does not evenly divide any of the array elements.

> **Note:** There are a few syntax issues in the current code, such as `lenght` instead of `length` and `! ===` instead of `!==`. These need to be corrected for the function to work properly.

## Parameters
- `inputArray` (`Array<number>`): An array of integers representing the positions of obstacles.

## Function Logic
1. **Sort the array:**  
   The array is sorted in ascending order to easily determine the largest obstacle.

   ```javascript
   inputArray = inputArray.sort((a, b) => a - b);




