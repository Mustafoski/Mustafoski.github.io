---
layout: post
title: "Has Only Even Number"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-01-12T15:39:55-04:00
modified: 2022-01-12T15:39:55-04:00
---

## Has Only EvenNumber

Even numbers are whole numbers that cannot be divided exactly into pairs. Odd numbers, when divided by 2, leave a remainder of 0. Even numbers have the digits 2, 4, 6, 8  in their ones place.

Example:<br>
console.log(hasOnlyEvenNumber([1,2,4,5])); true <br>
console.log(hasOnlyEvenNumber([1,3,5])); false  <br>




~~~
function hasOnlyEvenNumber(arr){
  return arr.some(function(val){
    return val % 2 === 0;
  })
}

let arr= [1,2,3,4,5,6,7,8,9,10];
console.log(hasOnlyEvenNumber(arr)); true

~~~
___
We create a function called hasOnlyEvenNumber with parameter called *arr* 
<br><br>
We return the *arr*.every every is build in JavaScript method that needs all to be true from the array
<br><br>
We return *arr*.some(function(val){ <br> 
  return val %  2 === 0}) <br>
This means that we take the *arr* argument use the some method and iterate and check if *val* % (remainder operator) 2 is equal to remainder 0;<br>
<br><br>
