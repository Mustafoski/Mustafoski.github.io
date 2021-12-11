---
layout: post
title: "Palindrom-v4"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-07-16T15:39:55-04:00
modified: 2021-07-16T15:39:55-04:00
---

## Palindrom v4


Given a string, return a new string with the reversed order of characters.

Example:<br>
console.log(checkPalindrom('hannah')) true <br>
console.log(checkPalindrom('apple'))  false <br>



~~~
function checkPalindrom(str) {
  str = str.toLowerCase();
  let first = str.split(' ').join('')
  let second = first.split('').reverse().join('')

  return first === second
}
console.log(checkPalindrom('hannah')) true 
console.log(checkPalindrom('apple'))  false 

~~~
___

We create a function checkPalindrom(str) parameter str. <br>
We turn the parameter into all characters in LowerCase with JavaScript build in method toLowerCase()<br>
We create variable first and we split the parameter with space then we join using JavaScript build in methods split() and join() <br>
We create another variable second that split the first variable without using space between reverse the order and join using the JavaScript build in methods split() reverse() join().
<br>
In the end we check with return if first is equal to second.


