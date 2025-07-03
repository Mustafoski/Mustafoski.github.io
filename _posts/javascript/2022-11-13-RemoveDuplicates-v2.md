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



The code is using a technique called "hash mapping" to remove duplicates from the input array. The idea is to use an object to store the unique elements of the array as properties, with the values being set to a constant value (in this case, 1). Since object properties must be unique, this ensures that no duplicates are added to the object.
<br><br>
Here's a step-by-step explanation of how the code works:
<br><br>
An empty object result is declared to store the unique elements of the array.
<br><br>
The for-of loop is used to iterate over each element x in the input array arr.
<br><br>
For each iteration of the loop, a new property is added to the result object with the name x and a value of 1.
<br><br>
If the same value appears multiple times in the input array, the code will still only add a single property with that value to the result object.
<br><br>
After the loop has finished, the Object.keys method is used to extract an array of all property names from the result object. This array contains all the unique elements from the input array.
<br><br>
Finally, the function returns this array as the result.
<br><br>
The two console.log statements log the results of calling the removeDuplicates function with two arrays arr1 and arr2. However, these arrays are not defined in the code snippet you provided, so the code would throw an error if run as-is. You need to define these arrays before calling the removeDuplicates function, like this:
<br><br>
const arr1 = [1, 2, 3, 1, 2, 3];
<br>
const arr2 = [1, 2, 3, 4, 5];
<br><br>
console.log(removeDuplicates(arr1)); 1,2,3
<br>
console.log(removeDuplicates(arr2)); 1,2,3,4,5
<br>