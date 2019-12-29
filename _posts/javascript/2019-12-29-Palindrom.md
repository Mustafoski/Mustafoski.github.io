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
date: 2019-12-29T15:39:55-04:00
modified: 2019-12-29T15:39:55-04:00
---

## Palindrom


Given a string, return a new string with the reversed order of characters.

Example:<br>
reverse('apple') = 'leppa'<br>
reverse('hello') = 'olleh'<br>
reverse('Greetings') = 'sgniteerG'<br>



~~~
function reverse(str) {
	return str.split('').every((char, i) => {
		return char === str[str.length - i -1];
		});
	}

~~~
___

For better explanation of this solution will be graphical 
A B C B A
every function works on arrays so we split(''). Then 
every checks in this order.
is A === A(last one) yes ok palindrom
is B === B(before last) yes ok palindrom
is C === C (C is only one )so palindrom.
But unfortunatelly 
the list goes on
is B ==== B(index 1) palindrom
is A ==== A (index 0) palindrom

