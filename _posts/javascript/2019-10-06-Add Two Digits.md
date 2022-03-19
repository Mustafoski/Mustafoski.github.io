---
layout: post
title: "Add Two Digits"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2019-12-22T15:39:55-04:00
modified: 2019-12-22T15:39:55-04:00
---

## Add Two Digitis

Outside of the values we give border with the style of *

___

> ##For Example
For n = 29 the output should be 2+9 =  return 11<br>

Should return true<br>
##
<br>

___


~~~
let n = 29;

function addTwoDigits(n){
  const nums = n.toString().split('');
  
  return nums.reduce((x, y) => {
    return parseInt(x)+ parseInt(y)
  })
}

console.log(addTwoDigits(n))

~~~

We create a function addTwoDigits with parameter **n** and local varable nums that is equal to **n.toString().split('')**
<br><br>
We convert **n** toString() which is build in JavScript method for converting to string and if we chain .split() we turn that string into an array.
<br>
The split() method divides a String into an ordered list of substrings, puts these substrings into an array, and returns the array. The division is done by searching for a pattern; where the pattern is provided as the first parameter in the method's call. -MDN
<br><br>
Lastly we return ***nums.reduce((x ,y) => {
  return parseInt(x) + parseInt(y)
})***
<br><br>
