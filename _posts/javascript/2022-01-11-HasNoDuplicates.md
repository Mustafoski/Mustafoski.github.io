---
layout: post
title: "HasNoDuplicates"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-01-11T15:39:55-04:00
modified: 2022-01-11T15:39:55-04:00
---

## Has No Duplicates

Has No Duplicates numbers are  numbers that cannot have duplicates, if there are duplicates we return false else we return true

Example:<br>
console.log(hasNoDuplicates([1,0,2,3,4,4])) false <br>
console.log(hasNoDuplicates([1,2,3,4,5,6])) true  <br>




~~~
function hasNoDuplicates(arr){
  return arr.every(function(val){
    return arr.indexOf(val) === arr.lastIndexOf(val)
  })
}

console.log(hasNoDuplicates([1,0,2,3,4,4])) false
console.log(hasNoDuplicates([1,2,3,4,5,6])) true


~~~
___
We create a function called hasNoDuplicates with parameter called *arr* 
<br><br>
We return the *arr*.every every is build in JavaScript method that needs all to be true from the array or not;
<br><br>
We return *arr*.every(function(*val*){ <br> 
  return *arr*.indexOf(*val*) === *arr*.lastIndexOf(*val*) <br>
After returning .every we have callback function with paramerer *val* and we return the indexOf which is JavaScript method The indexOf() method returns the first index at which a given element can be found in the array, or -1 if it is not present. -MDN 
<br><br>
To be equal to *arr*.lastIndexOf(*val*) which is another JavaScript method The lastIndexOf() method returns the last index at which a given element can be found in the array, or -1 if it is not present. The array is searched backwards, starting at fromIndex. -MDN
<br><br>
If indexOf and lastIndexOf the parameter *val* are found in both of the methods it returns false; if every index is different is returns true;
