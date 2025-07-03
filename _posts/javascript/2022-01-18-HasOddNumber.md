---
layout: post
title: "HasOddNumber"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-01-18T15:39:55-04:00
modified: 2022-01-18T15:39:55-04:00
---

## HasOddNumber

Odd numbers are whole numbers that cannot be divided exactly into pairs. Odd numbers, when divided by 2, leave a remainder of 1. 1, 3, 5, 7, 9, 11, 13, 15 … are sequential odd numbers. Odd numbers have the digits 1, 3, 5, 7 or 9 in their ones place.

Example:<br>
console.log(hasOddNumber([1,2,4,5])); true <br>
console.log(hasOddNumber([2,4,6])); false  <br>





~~~
function hasOddNumber(arr){
  return arr.some(function(val){
    return val % 2 !== 0;
  })
}

let arr= [1,2,3,4,5,6,7,8,9,10];
console.log(hasOddNumber(arr)); true

~~~
___
We create a function called hasOddNumber with parameter called *arr* 
<br><br>
We return the *arr*.some some is build in JavaScript method that only one needs to be true from the array;
<br><br>
We return *arr*.some(function(val){ <br> 
  return val %  2 !== 0}) <br>
This means that we take the *arr* argument use the some method and iterate and check if *val* % (remainder operator) 2 is different than 0;<br>
<br><br>
