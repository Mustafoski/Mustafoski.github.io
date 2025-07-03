---
layout: post
title: "Add Key and Value"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-01-22T15:39:55-04:00
modified: 2022-01-22T15:39:55-04:00
---

## Add Key and Value

Write a function called addKeyAndValue which accepts an array of objects and returns the array of objects passed to it with each object now including the key and value passed to the function.

Example:<br>
var arr = [{name: 'Elie'}, {name: 'Tim'}, {name: 'Matt'}, {name: 'Colt'}];<br>
console.log(JSON.stringify(addKeyAndValue(arr, 'title', 'Instructor'),null,2)) <br>
"[<br>
  {<br>
    \"name\": \"Elie\",<br>
    \"title\": \"Instructor\"<br>
  },<br>
  {<br>
    \"name\": \"Tim\",<br>
    \"title\": \"Instructor\"<br>
  },<br>
  {<br>
    \"name\": \"Matt\",<br>
    \"title\": \"Instructor\"<br>
  },<br>
  {<br>
    \"name\": \"Colt\",<br>
    \"title\": \"Instructor\"<br>
  }<br>
]"<br>





~~~
function addKeyAndValue(arr, key, value){

    return arr.reduce(function(acc, next, idx){ 

      acc[idx][key] = value;
      return acc;

}, arr);
 
}

 var arr = [{name: 'Elie'}, {name: 'Tim'}, {name: 'Matt'}, {name: 'Colt'}];

    

 console.log(JSON.stringify(addKeyAndValue(arr, 'title', 'Instructor'),null,2))
~~~
___
We create a function called addKeyAndValue and we create parameter  *arr* and  *key* and *value*
<br><br>
We return *arr*.reduce(function(acc,next,idx) {}) *arr* is an array that hold key value pairs inside and with reduce we chain .reduce and have callback function that accepts mostly 2 cases buy in our case we need the index case. those are acc,next,idx
<br><br>
 acc[idx][key] = value; We take the key value pair of some index acc holds all the data , [idx] gives specivic index we need and from that data and that index we have that [key] and it will equal to value;
<br><br>
 return acc; We return corrected key value paird new *acc* or accumulator 
<br><br>



