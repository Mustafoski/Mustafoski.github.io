---
layout: post
title: "Array Max Consecutive Sum"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2023-02-08T15:39:55-04:00
modified: 2023-02-08T15:39:55-04:00
---

Array Max Consecutive Sum
<br><br>

Given an array of integers, find the maximal possible sum of some of its k consecutive elements.

**Example**<br>
let inputArray = [2,3,5,1,6]; and **k** is 2 The output should ne arrayMaxConsecutiveSum(inputArray,k) => 8.
<br><br>
All possible sums of 2 consecutive elements are <br>
* 2 + 3 = 5;<br>
* 3 + 5 = 8;<br>
* 5 + 1 = 6;<br>
* 1 + 6 = 7;<br>



~~~
function arrayMaxConsecutiveSum(inputArray = [], k) {
  let sum = 0;
  let max = 0;
  
  for(let i = 0;i < k;i++){
      sum+= inputArray[i];
  }
  max = sum;
  
  for (let i = k; i < inputArray.length; i++) {
    sum -= inputArray[i-k];
    sum += inputArray[i];
    
    if (sum > max ) {
      max = sum;
    }
  }
  
  
  return max;
}

console.log(arrayMaxConsecutiveSum([2,3,5,1,6],2));
~~~



The function arrayMaxConsecutiveSum takes in two arguments: inputArray which is an array of numbers, and k which is a positive integer. The function calculates the maximum sum of k consecutive elements in inputArray.
<br><br>
The algorithm for the function is as follows:
<br><br>
1. Initialize two variables, sum and max to 0. sum will keep track of the current sum of k consecutive elements, and max will keep track of the maximum sum found so far.
<br><br>
2. The first loop runs from 0 to k-1, and adds the first k elements of inputArray to sum. At the end of the loop, sum contains the sum of the first k elements in inputArray, and max is set to sum since this is the maximum sum found so far.
<br><br>
3. The second loop runs from k to the end of the inputArray. In each iteration, sum is updated by subtracting the value of the k-th element before the current k elements and adding the value of the current k-th element. The updated sum is then compared to max, and if it is greater, max is updated to sum.
<br><br>
4. Finally, the function returns the value of max, which is the maximum sum of k consecutive elements in inputArray.
<br><br>
Example: arrayMaxConsecutiveSum([2,3,5,1,6],2).
<br><br>
sum = 2 + 3 = 5
<br><br>
max = sum = 5
<br><br>
On the first iteration of the second loop, sum = sum - 2 + 5 = 8
<br>
max is updated to sum = 8
<br><br>
On the second iteration of the second loop, sum = sum - 3 + 1 = 6
<br>
max remains 8 since 6 is not greater than 8.
<br><br>
The function returns 8 which is the maximum sum of 2 consecutive elements in [2,3,5,1,6].