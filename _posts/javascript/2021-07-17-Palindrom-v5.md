---
layout: post
title: "Palindrom-v5"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-07-17T15:39:55-04:00
modified: 2021-07-17T15:39:55-04:00
---

## Palindrom v5


Given a string, return a new string with the reversed order of characters.

Example:<br>
console.log(checkPalindrom('hannah')) true <br>
console.log(checkPalindrom('apple'))  false <br>



~~~
function checkPalindrom(str) {
  let tempStr = str.match(/[a-z0-9]+/ig).join('').toLowerCase()
  console.log(tempStr) 

  let second = tempStr.split('').reverse().join('')
  console.log(second)


  return tempStr === second;
}

console.log(checkPalindrom('hannah')) true 
console.log(checkPalindrom('apple'))  false 
}

~~~
___

We create a function checkPalindrom(str) parameter str. <br>
We turn the parameter into all characters in regex function with match method  JavaScript build in method match()<br>

We use (/[a-z0-9]+/ig) => we check from a - z and 0 - 9; i = ignores casing ; g = global; + = returns the repetitions <br>

We chained Javascript build in method join() and toLowerCase() <br>
We create another variable second that split the tempStr variable without using space between reverse the order and join using the JavaScript build in methods split() reverse() join().
<br>
In the end we check with return if tempStr is equal to second.


