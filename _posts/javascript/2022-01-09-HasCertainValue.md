---
layout: post
title: "Has Certain Value"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-01-09T15:39:55-04:00
modified: 2022-01-09T15:39:55-04:00
---

## Has Certain Value
Write a function called hasCertainV
alue which accepts an array of objects and a key, and a value, and returns true if every single object in the array contains that value for the specific key. Otherwise it should return false.

Example:<br>
console.log(hasCertainValue(arr, "first", 'Elie')) // false <br>
console.log(hasCertainValue(arr,'title','Instructor')) // true <br>





~~~
function hasCertainValue(arr, key, searchValue){
  return arr.every(function(val){
    return val[key] === searchValue;
  })
}


var arr = [

        {title: "Instructor", first: 'Elie', last:"Schoppik"}, 

        {title: "Instructor", first: 'Tim', last:"Garcia", isCatOwner: true}, 

        {title: "Instructor", first: 'Matt', last:"Lane"}, 

        {title: "Instructor", first: 'Colt', last:"Steele", isCatOwner: true}

    ];
console.log(hasCertainValue(arr, "first", 'Elie')) // false
console.log(hasCertainValue(arr,'title','Instructor')) // true

~~~
___
We create a function called HasCertainValue with parameter called *arr* and *key* and *searchValue*
<br><br>
We return the *arr*.every every is build in JavaScript method that needs all to be true from the array or not;
<br><br>
Then inside every method we invode callback function with parameter *val* to 
 ***return *val*[*key*] === *searchValue***
<br><br>
We return the *val[key]* of all key members and triple equal or strict equal to *searchValue*
<br><br>
We still loop throuh every method and ***return *val*[*key*] === *searchValue*** is checking if val[key] === searchValue (searchValue we provide as value of key-value pair) so while checking with every that everything must be true it returns true else false;
<br><br>
As I said above every method needs all of them to be true to be true so the *key* had to have the same value in all array objects *arr* that is possible in the case in the console log method.
