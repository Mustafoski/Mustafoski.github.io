---
layout: post
title: "Cars Passing"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-12-02T15:39:55-04:00
modified: 2021-12-02T15:39:55-04:00
---

## Cars Passing

A non-empty zero-indexed array A consisting of N integers is given. The consecutive elements of array A represent consecutive cars on a road.The goal is to count passing cars. We say that a pair of cars (P, Q), where 0 ≤ P < Q < N, is passing when P is traveling to the east and Q is traveling to the west.

Example:<br>
console.log(PassingCars([0,1,0,1,1])); -> 5<br>




~~~
function PassingCars(inputArray) {
  let suffixSum = new Array(inputArray.length + 1).fill(0);
  let count = 0;

for (let i = inputArray.length - 1; i >= 0; i--) {
  suffixSum[i] = inputArray[i] + suffixSum[i + 1];
  if (inputArray[i] === 0) count += suffixSum[i];
  if (count > 1000000000) return -1;
}

return count;
}

console.log(PassingCars([0,1,0,1,1])); -> 5

~~~
___
We create a function called CarsPassing with parameter called *inputArray* we create an variable called *suffixSum* and it will be an array with size of *inputArray.length + 1* and initially we fill the array with 0. Next we create varible  *count* that we initialize to 0;
<br><br>
We create for loop where we start with *i* = *inputArray.length - 1*, second condition is *i* is bigger or equal to 0 and third condition is where we decrement i by 1;
<br><br>
The way we compute the *suffixSum* is to write *suffixSum[i] = inputArray[i] + suffixSum[i + 1];*
*suffixSum* one position more than i and i + 1 is the reason why we have created the suffixSum to be one position bigger than our inputs.
<br><br>
And in this way the suffix sum area is kindd of a table containing the numbers of cars that are still in front of us for each position.
<br><br>
Next we have if statement *if (inputArray[i] === 0) count += suffixSum[i]* Meaning that the car is traveling EAST we need to update the count variable with count += suffixSum[i]
<br><br>
Final thing we have to do is another if statement *if (count > 1000000000) return -1;* If the count is bigger than 1,000,000,000 we return -1;  
<br> <br> 
In the end we return count;
 

