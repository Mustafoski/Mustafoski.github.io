---
layout: post
title: "Reverse String-v8"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-01-21T15:39:55-04:00
modified: 2022-01-21T15:39:55-04:00
---

## Reverse String-v8

Reverse String can be defined as an operation in which the original string which the user gives is modified in such a way that the characters in it are arranged in a reverse manner starting from the last character to the first character, thus by forming a new string which will be the exact reverse of the original

Example:<br>
var str = new String('emir').reverse(); => rime <br>
console.log(str) => rime <br>





~~~
function reverse(value) {
  let result = ''
  
  let array = value.split('').length
  for (let i =0;i<array;i++){

    result = value[i] + result
  }
  return result;
}
console.log(reverse('emir')) => rime
~~~
___
We create a function called reverse and we create parameter  *value* and variable *result*='' 
<br><br>
Then we created another variable *array* to be equal to *value*.split('').length<br>
.split('') will split the string into an array and .length checks the lenght
<br><br>
We loop from 0 until the end of the newly formed array called *array* and we increment by 1
<br><br>
***result = value[i] + result*** 
<br><br>
The empty initially variable *result* will take the first r and the rest of the string
<br><br>
In the end we ***return result***


