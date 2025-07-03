---
layout: post
title: "Palindrom"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2019-10-06T15:39:55-04:00
modified: 2019-10-06T15:39:55-04:00
---

## Palindrom

A palindrome is a word, number, phrase, or other sequence of characters which reads the same backward as forward, such as ‘’taco cat’’ or madam or racecar or the number 10801


Given a string, return true if the string is a palindrome or false if it is not.

##For Example
console.log(reverse('hannah')) true <br>
console.log(reverse('apple'))  false <br>
<br>

~~~
function palindrome(str) {
	const reversed = str.split('').reversed().join('');
	return str === reversed
}
console.log(reverse('hannah')) true <br>
console.log(reverse('apple'))  false <br>
~~~


1. Split the string with split('') that gives me an array that I will reverse().<br>
2. Then i will chain the reverse() method to split('').reversed() which in turn will reverse the letters.<br>
3. After that i will chain .join('') which is used to join the elements of an array into a string.<br>
4. Finally if parameter <strong>str</strong> is strong equal to reversed we return it.It will be eather true or false depending on the tests. <br>