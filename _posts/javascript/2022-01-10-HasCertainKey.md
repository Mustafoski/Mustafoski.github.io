---
layout: post
title: "Has Certain Key"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-01-10T15:39:55-04:00
modified: 2022-01-10T15:39:55-04:00
---

## Has Certain Key
In nested objects if all of the keys have same key it returns true if some of them do not have 
it returns false;

Example:<br>
console.log(hasCertainKey(arr,'isCatOwner')) false <br>
console.log(hasCertainKey(arr,'title')) true <br>
console.log(hasCertainKey(arr,'first')) true <br>





~~~
function hasCertainKey(arr, key){
  return arr.every(function(val){
    return key in val
  })
}

  var arr = [

        {title: "Instructor", first: 'Elie', last:"Schoppik"}, 

        {title: "Instructor", first: 'Tim', last:"Garcia", isCatOwner: true}, 

        {title: "Instructor", first: 'Matt', last:"Lane"}, 

        {title: "Instructor", first: 'Colt', last:"Steele", isCatOwner: true}

    ]
console.log(hasCertainKey(arr,'isCatOwner')) false
console.log(hasCertainKey(arr,'title')) true
console.log(hasCertainKey(arr,'first')) true

~~~
___
We create a function called hasCertainKey with parameter called *arr* and *key*
<br><br>
We return the *arr*.every every is build in JavaScript method that needs all to be true from the array or not;
<br><br>
Then return *key* in *val* The in operator returns true if the specified property is in the specified object or its prototype chain. -MDN
<br><br>

<br><br>

