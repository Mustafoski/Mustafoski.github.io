---
layout: post
title: "Palindrom-v6"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-12-12T15:39:55-04:00
modified: 2021-12-12T15:39:55-04:00
---

## Palindrom v6


Given a string, return a new string with the reversed order of characters.

Example:<br>
console.log(checkPalindrom('hannah')) true <br>
console.log(checkPalindrom('apple'))  false <br>



~~~
function palindrom(str){
  return str.split('').reverse().join('') === str ? true : false;
}

console.log(palindrom('hannah')) 
console.log(checkPalindrom('apple'))
~~~
___

We create a function palindrom(str) parameter str. 
<br>
We return str.split('') to turn the string into an array
<br>
We chain .reverse() to reverse the letters of the array
<br>
We chain .join('') to join the letters into string
<br>
We chech with === if all above functions are reversing the string and check with original like this === str
<br>
Then we use ternery operation if it is true *?* we return true *:* false
<br>



