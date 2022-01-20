---
layout: post
title: "Has Only Odd Number"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-01-13T15:39:55-04:00
modified: 2022-01-13T15:39:55-04:00
---

## Has Only Odd Number

Odd numbers are whole numbers that cannot be divided exactly into pairs. Odd numbers, when divided by 2, leave a remainder of 1. 1, 3, 5, 7, 9, 11, 13, 15 … are sequential odd numbers. Odd numbers have the digits 1, 3, 5, 7 or 9 in their ones place.

Example:<br>
console.log(hasOnlyOddNumbers([1,3,5])) true <br>
console.log(hasOnlyOddNumbers([1,3,4])) false <br>





~~~
function hasOnlyOddNumbers(arr){
  return arr.every(function(val){
    return val % 2 !== 0;
  })
}
console.log(hasOnlyOddNumbers([1,3,5])) true
console.log(hasOnlyOddNumbers([1,3,4])) false

~~~
___
We create a function called hasOnlyOddNumbers with parameter called *arr* 
<br><br>
We return the *arr*.every every is build in JavaScript method that needs all to be true from the array or not;
<br><br>
We return *arr*.every(function(val){ <br> 
  return val %  2 !== 0}) <br>
This means that we take the *arr* argument use the some method and iterate and check if *val* % (remainder operator) 2 is different than 0;<br>
<br><br>
