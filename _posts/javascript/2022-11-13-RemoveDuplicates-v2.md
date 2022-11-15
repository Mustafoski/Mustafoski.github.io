---
layout: post
title: "Remove Duplicates v2"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-11-13T15:39:55-04:00
modified: 2022-11-13T15:39:55-04:00
---

Remove Duplicates v2
<br><br>

Given an array find and remove Duplicates

**Example**<br>
let arr1 = [1, 1, 2, 3, 3, 100, 3, 7, -4]; => [ '1', '2', '3', '7', '100', '-4' ]
let arr2 = ['Hi', 'Hello', 'Hi', 'Hey','Hi']; => [ 'Hi', 'Hello', 'Hey' ]




~~~
function removeDuplicates(arr) {
  let result = {};

  for (let x of arr) {
    result[x] = 1;
  }
  return Object.keys(result);
}

console.log(removeDuplicates(arr1))
console.log(removeDuplicates(arr2))
~~~



We create function called removeDuplicates with parameter *arr* and local variable **result = {}**
<br><br>
We loop the array given into the parameter *arr* with while loop with for of loop ***for(let x of arr)***
<br><br>
Inside the for loop we check **result[x] = 1** 
<br><br>
In the end we **return Object.keys(result)** but the keys of numbers are converted to strings if we want to change that we can chain .map(x => Number(x)) but the arr2 with the strings will be Nan Nan Nan
