---
layout: post
title: "Palindrom-v5"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-07-17T15:39:55-04:00
modified: 2021-07-17T15:39:55-04:00
---

## Palindrom v5


Given an array of 2k integers we perfrom the following operations until the array contains only one element.
1. On the 1st,3rd,5th etc. iterations (1-based) replace each pair of consecutive elements with their sum. <br>
2. On the 2nd,4th,6th etc. iterations replace each pair of consecutive elements with their product.

After the algorithm has finished, there will be a single element left in the array. We return that element.

Example:<br>
console.log(ArrayConvertion([1,2,3,4,5,6,7,8])) 186 <br>




~~~
function ArrayConvertion(inputArray) {
  let isOdd = true;

  while(inputArray.length !== 1) {
    inputArray = sumProduct(inputArray,isOdd)
    isOdd = !isOdd;
  }
  return inputArray[0];
  
}

function sumProduct(nums,isOdd) {
  const sumProducts = [];
  if (isOdd) {
    for (let i = 0; i<nums.length;i+=2) {
      sumProducts.push(nums[i] + nums[i+1])
    }
  } else {
    for (let i = 0; i<nums.length;i+=2) {
      sumProducts.push(nums[i] * nums[i+1])
    }
  }
  return sumProducts;
}

console.log(ArrayConvertion([1,2,3,4,5,6,7,8])) 186
}

~~~
___

We create a function ArrayConversion with parameter of inputArray and we create a variable isOdd to be equal to true so we can keep track if the element is odd or even <br>
We loop with while loop throuh the inputArray until the length is different than 1 (because as the algorithm suggest only one element remains as result) <br>
We initialize inputArray to a function sumProduct that takes for arguments inputArray and isOdd then
we switch isOdd to is not !isOdd
<br>
Function SumProduct takes as we said above two arguments nums array and boolean isOdd and also we create a variable to hold the sum and product of the array numbers.
 <br>
 We check if isOdd and if it is Odd we loop from 0 to the array length skipping one by doing
 for(let i = 0; i < nums.legth; i+= 2) 
 Then we use sumProduct and push the first iteration (num[i]) + second iteration (num[i+1])
<br>
else if it is Even we  loop from 0 to the array length skipping one by doing
 for(let i = 0; i < nums.legth; i+= 2) 
 Then we use sumProduct and push the first iteration (num[i]) * second iteration (num[i+1]) <br>
We return the sumProduct 
<br>
And in the ArrayConversion function we return inputArray[0] 


