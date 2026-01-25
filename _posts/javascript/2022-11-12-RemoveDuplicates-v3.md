---
layout: post
title: "Remove Duplicates v3"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-11-12T15:39:55-04:00
modified: 2022-11-12T15:39:55-04:00
---

Remove Duplicates v3
<br><br> 

Given an array find and remove Duplicates

**Example**<br>
let arr1 = [1, 1, 2, 3, 3, 100, 3, 7, -4]; => [ 1, 2, 3, 100, 7, -4 ]
let arr2 = ['Hi', 'Hello', 'Hi', 'Hey','Hi']; => [ 'Hi', 'Hello', 'Hey' ]




~~~
function removeDuplicates(arr) {
 return [...new Set(arr)];
}

console.log(removeDuplicates(arr1))
console.log(removeDuplicates(arr2))

~~~



We create function called removeDuplicates with parameter *arr*
<br><br>
We use Set functions to remove duplicates 
<br><br>
***return[...new Set(arr)];
<br><br>
