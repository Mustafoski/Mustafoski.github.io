---
layout: post
title: "Max Profit"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-11-29T15:39:55-04:00
modified: 2021-11-29T15:39:55-04:00
---

## Max Profit

We sum the elements from the array and we move in every item and we choose the bigger from the last sum and the next index and if the next item is smaller than the last sum we continue with the last sum then we continue with the next items in the array, in the end we choose the biggest global max value.

Example:<br>
console.log(MaxProfit([23171,21011,21123,21366,21013,21367])); -> 356 <br>




~~~
function MaxProfit(array) {
  let globalMaxSum = 0;
  let localMaxSum = 0;

  for (let i = 1; i < array.length; i++) {
    let d = array[i] - array[i - 1];
    localMaxSum = Math.max(d,localMaxSum + d);
    globalMaxSum = Math.max(localMaxSum,globalMaxSum);
  }
  return globalMaxSum;
}

console.log(MaxProfit([23171,21011,21123,21366,21013,21367])); -> 356

~~~
___
We create a function called MaxProfit with parameter called *array* we create an variable called    *globalMaxSum* and variable *localMaxSum* that we initialize to 0;
<br><br>
We loop with for of loop for(let i = 1; i < array.length;i++) The reason we start from the second position from i is equal to one istead of 0 is that we want to find the difference between each element and it's previous one.<br><br>
Then we create variable *d* representing the difference is equals to array[i] - array[i - 1];
We subtracted from the previous day and this is the reason why we start from position one and not zero.
<br><br>
Next we need to update our locallMaxSum variable and we set it to be using JavaScript build in method Math.max and we use Math.max(d, localMaxSum + d)<br>
We set it to be maximum between the *d* or localMaxSum + d we make this choice over here to whatever is bigger;
<br><br>
Then we update *globalMaxSum* and we update it to the value of the maximum between the *localMaxSum* and the *globalMaxSum* by using again the Math.max(localMaxSum, globalMaxSum)
<br> <br> 
In the end of this loop we just return the solution which will be contained in *globalMaxSum* this will represent the sum of the maximum subarray which in this particular puzzle it will also represent the maximum profit that we can achieve from our input prices.<br>
return globalMaxSum;
 

