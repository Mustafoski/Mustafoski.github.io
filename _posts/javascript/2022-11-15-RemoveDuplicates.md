---
layout: post
title: "Remove Duplicates"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-11-15T15:39:55-04:00
modified: 2022-11-15T15:39:55-04:00
---

Remove Duplicates
<br><br>

Given an array find and remove Duplicates

**Example**<br>
let arr1 = [1, 1, 2, 3, 3, 100, 3, 7, -4]; => [ 1, 2, 3, 100, 7, -4 ]
let arr2 = ['Hi', 'Hello', 'Hi', 'Hey','Hi']; => [ 'Hi', 'Hello', 'Hey' ]




~~~
function removeDuplicates(arr) {
  let result = [];

  for (let x of arr) {
    if (!result.includes(x)) {
      result.push(x)
    }
  }
  return result;
}

console.log(removeDuplicates(arr1))
console.log(removeDuplicates(arr2))

~~~



We create function called removeDuplicates with parameter *arr* and local variable **result = []**
<br><br>
We loop the array given into the parameter *arr* with while loop with for of loop ***for(let x of arr)***
<br><br>
Inside the for loop we check  if(!result.includes(x)) and if true **result.push(x)**
<br><br>
In the end we **return result**
