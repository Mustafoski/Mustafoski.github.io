---
layout: post
title: "Palindrom-v2"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-12-11T15:39:55-04:00
modified: 2021-12-11T15:39:55-04:00
---

## Palindrom v2


Given a string, return a new string with the reversed order of characters.

Example:<br>

console.log(reverse('hannah')) true <br>
console.log(reverse('apple'))  false <br>

~~~
function reverse(str) {
	return str.split('').every((char, i) => {
		return char === str[str.length - i -1];
		});
	}
console.log(reverse('hannah'))
console.log(reverse('apple'))
~~~
___

For better explanation of this solution will be graphical <br>
A B C B A<br>
every function works on arrays so we split(''). Then <br>
every checks in this order.<br>
is A === A(last one) yes ok palindrom<br>
is B === B(before last) yes ok palindrom<br>
is C === C (C is only one )so palindrom.<br>
But unfortunatelly <br>
the list goes on<br>
is B ==== B(index 1) palindrom<br><br>
is A ==== A (index 0) palindrom<br>

