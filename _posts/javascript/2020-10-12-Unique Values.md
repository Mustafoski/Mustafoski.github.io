---
layout: post
title: "Unique Values"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2020-10-12T15:39:55-04:00
modified: 2020-10-12T15:39:55-04:00
---

## Unique Values

Unique Values is when in a string every letter is unique if they are all different unique then it is true of not like the second example if there are duplicates than it is false.

___

> ##For Example<br>
  abcde => true<br>
 abcda => false<br>
>
##
<br>

___

~~~

 function uniqueValues(str) {
  let values = [];

  for(let letter of str){
    if(values.indexOf(letter) !== -1){
      return false;
    }
    values.push(letter);
  }
  return true;
}
console.log(uniqueValues('abcde')) true
console.log(uniqueValues('abcdea')) false two 'a'
~~~

function uniqueValues(str) { <br><br>
First we create a function called uniqueValues and pass an argument called string.<br><br>
let values = []; 

First and foremost we are going to create variable to hold an array and initiate to empty array<br><br>
for(let letter of str){
  if(values.indexOf(letter) !== -1){
  return false;
  }
  values.push(letter)
}
return true <br><br>

We create a for of loop to loop through the array of the parameter and then we check with indexOf method if the index of letter is -1. if it is not -1 we return false if it is -1 we use the push method and push to values array.<br><br>

console.log(uniqueValues('abcde') true all unique<br><br>
console.log(uniqueValues('abcdea')) false two 'a'
