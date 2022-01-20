---
layout: post
title: "HasEvenNumber"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-01-14T15:39:55-04:00
modified: 2022-01-14T15:39:55-04:00
---

## HasEvenNumber

Even numbers are whole numbers that cannot be divided exactly into pairs. Odd numbers, when divided by 2, leave a remainder of 0. Even numbers have the digits 2, 4, 6, 8  in their ones place.

Example:<br>
console.log(hasOddNumber([1,2,4,5])); true <br>
console.log(hasOddNumber([2,4,6])); false  <br>




~~~
function hasEvenNumber(arr){
  return arr.some(function(val){
    return val % 2 === 0;
  })
}

let arr= [1,2,3,4,5,6,7,8,9,10];
console.log(hasOddNumber(arr)); true

~~~
___
We create a function called hasEvenNumber with parameter called *arr* 
<br><br>
We return the *arr*.some some is build in JavaScript method that only one needs to be true from the array;
<br><br>
We return *arr*.some(function(val){ <br> 
  return val %  2 === 0}) <br>
This means that we take the *arr* argument use the some method and iterate and check if *val* % (remainder operator) 2 is equal to remainder 0;<br>
<br><br>
