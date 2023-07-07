---
layout: post
title: "Array Maximal Adjacent Difference"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2023-02-13T15:39:55-04:00
modified: 2023-02-13T15:39:55-04:00
---

Array Maximal Adjacent Difference 
<br><br>

Given an integer, find the maximal absolute difference between any two of its adjacent elements.
**Example**<br>
For Input: inputArray = [2, 4, 1, 0] the output should be arrayMaximalAdjacentDifference(inputArray) = 3
<br>
Solution: 20
<br>
console.log(double(10,2)) => 40
<br>

~~~
function arrayMaximalAdjacentDifference(inputArray) {
  let maxDiff = Math.abs(inputArray[0] - inputArray[1]);
  
  for(let i = 0; i< inputArray.length; i++) {
    let absoluteDiff = Math.abs(inputArray[i-1]-inputArray[i]);
    
    maxDiff = absoluteDiff > maxDiff ? absoluteDiff : maxDiff;
  }
  
  return maxDiff;
}

console.log(arrayMaximalAdjacentDifference([2,4,1,0])) => 3
~~~



We have a function called ***arrayMaximalAdjacentDifference*** with parameters *inputArray*  and local variable *maxDiff* = ***Math.abs(inputArray[0] - inputArray[1]);***<br><br>

Then we iterate using for loop and create another temporary variable ***absoluteDiff = Math.abs(inputArray[i-1]-inputArray[i]);***
<br><br>
We check if maxDiff is equal to absoluteDiff lower than maxDiff and if true we return absoluteDiff else maxDiff;
<br><br>
In the end we ***return maxDiff***
