---
layout: post
title: "Reverse String-v4"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-11-17T15:39:55-04:00
modified: 2021-11-17T15:39:55-04:00
---

## Reverse String-v4

Given an expression string exp, write a program to examine whether the pairs and the orders of “{“, “}”, “(“, “)”, “[“, “]” are correct in exp.

Example:<br>
var str = new String('emir').reverse(); => rime <br>
console.log(str) => rime <br>





~~~
String.prototype.reverse = function() {
  var newStr = '';
  for(let i = this.length -1; i >= 0; i--) {
    newStr += this[i]
  }
  return newStr;
}

var str = new String('emir').reverse(); => rime
console.log(str) => rime
~~~
___
We create a String Prototype.reverse to be equal a function and we create a variable *newStr* = ''
<br><br>
We use for loop to go from i to the end of the string; this can be done with this.length -1<br>
Then we loop until i is bigger or equal to 0 <br>
In the end we decremenet by 1 with i-- <br>
<br><br>
Inside the loop we use *newStr* += this[i] it means *newStr* is appending to the current *i* 
<br><br>
At the end of the Prototype we return *newStr*
<br><br>
Outside the loop we create a variable *str* = new String('emir').reverse();<br>
Variable *str* is to hold the value of the new instance of String with parameter of string 'emir' (my name) and we chain .reverse(); to reverse it
<br>


