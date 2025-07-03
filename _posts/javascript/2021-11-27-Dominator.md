---
layout: post
title: "Dominator"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-11-27T15:39:55-04:00
modified: 2021-11-27T15:39:55-04:00
---

## Dominator

The problem is to find the dominant value in the input of array.

Example:<br>
console.log(Dominator([3,0,1,1,4,1,1])); 6 (index 6 that is value 1)<br>
console.log(Dominator([1,2,3,4,5,6,7])); -1 (because we dont have single leader)<br>




~~~
function Dominator(A) {
  let consecutiveSize = 0;
  let candidate = 0;

  A.forEach(item => {
    if (consecutiveSize === 0) {
      candidate = item;
      consecutiveSize += 1;
    } else if (candidate === item) {
      consecutiveSize += 1;
    } else {
      consecutiveSize -= 1;
    }
  })
  let occurence = 0;
  let index = 0;
  for(let i = 0; i < A.length; i++) {
    if (A[i] === candidate){
      occurence ++;
      index = i;
    }
  }
  return occurence > A.length / 2.0 ? index : -1;
}

console.log(Dominator([3,0,1,1,4,1,1]));
console.log(Dominator([1,2,3,4,5,6,7]));

~~~
___
We create a function called Dominator with parameters called A and we create an variable called consecutiveSize = 0 and candidate = 0;
<br>
We loop with forEach loop A.forEach(item => { -> to deal with number of cases <br>
  if (consecutiveSize === 0) { <br>
  we need to choose new candicate so  <br>
  candidate = item and consecutiveSize is incremented by 1 <br>
} else if (candidate === item) { <br>
  consecutiveSize is 0 and candidate is equal to item <br>
  We need just to increase the consecutiveSize by 1 <br>
} else { <br>
  In this case we have met an item that is different than the candidate that we are considering <br>
  In this case just substract consecutiveSize by 1 <br>
} <br>
}) <br>
<br>
We create two more variables occurence = 0 and index = 0; Remember we need to return the index of the leader of our array.
<br>
We create another for loop for(let i = 0; i < A.length; i++) { -> this is just to iterate over the input list <br>
  Inside the loop we check if (A[i] === candidate) {
  We increment the occurence and record the index that might return as a solution to this problem at the end <br>
}<br>
}<br>
<br>
In the end if the occurence is greater than A.length / 2.0 ? (we return ) index : (else) -1;
<br>
