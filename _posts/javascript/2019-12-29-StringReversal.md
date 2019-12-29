---
layout: post
title: "Reverse String-v2"
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

## Reverse String


Given a string, return a new string with the reversed order of characters.

Example:<br>
reverse('apple') = 'leppa'<br>
reverse('hello') = 'olleh'<br>
reverse('Greetings') = 'sgniteerG'<br>



~~~
function reverse(str) {
	let reversed = '';

	for (let character of str) {
		reversed = character + reversed;
	}
	return revesed
}

~~~
___

Create an empty string called reversed</br>
For each character in the provided string </br>
Take the character and add it to the start of reversed</br>
At Last we return the variable reversed</br>
