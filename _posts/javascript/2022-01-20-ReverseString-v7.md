---
layout: post
title: "Reverse String-v7"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-01-20T15:39:55-04:00
modified: 2022-01-20T15:39:55-04:00
---

## Reverse String-v

Reverse String can be defined as an operation in which the original string which the user gives is modified in such a way that the characters in it are arranged in a reverse manner starting from the last character to the first character, thus by forming a new string which will be the exact reverse of the original

Example:<br>
var str = new String('emir').reverse(); => rime <br>
console.log(str) => rime <br>





~~~
function reverse(s){
    return [...s].reverse().join("");
}

console.log(reverse('emir')) rime
~~~
___
We create a function called reverse and we create parameter  *s* 
<br><br>
We return [...s].reverse().join("")
<br><br>
We split the string to an array with spread operator with [...s]
<br><br>
We chain .reverse() to reverse the order of the newly formed array
<br><br>
We chain .join("") to concat the reversed array into string
<br>


