---
layout: post
title: "Almost Increasing Sequence"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-03-09T15:39:55-04:00
modified: 2022-03-09T15:39:55-04:00
---

Almost Increasing Sequence
<br>
Given a sequence of integers as an array, determine whether it is possible to obtain a strictly increasing sequence by removing no more than one element from the array.


**Example**<br>
- For sequence = [1, 3, 2, 1], the output should be<br>
almostIncreasingSequence(sequence) = false;<br>
- For sequence = [1, 3, 2], the output should be<br>
almostIncreasingSequence(sequence) = true.<br>
<br>




~~~
function almostIncreasingSequence(sequence){
  let count = 0;
  for(let i = 0; i< sequence.length;i++) {
    if (sequence[i] <= sequence[i - 1]){
      count++;
    
    if (sequence[i] <= sequence[i - 2] && sequence[i + 1] <= sequence[i-1]){
      return false
    }
  }
}
 return count <= 1;
}

console.log(almostIncreasingSequence([1, 3, 2, 1])) false 
console.log(almostIncreasingSequence([1, 3, 2])) true

~~~

___

We create function called adjacentElementsProduct with parameter **inputArray** and local variable **largestProduct** that is equal to **inputArray** = **inputArray[0] * **inputArray**c
<br><br>
**count** variable will hold how many times the sequence has been out of sync. We iterate into the array with for loop and check if *sequence[i]* <= *sequence[i - 1]* if true we increase **count++**
<br><br>
After that we check if *sequence[i]* <= *sequence[i - 2]* and *sequence[i + 1]* <= *sequnece[i - 1]*
we return false
<br><br>
In the end we **return count <= 1 **