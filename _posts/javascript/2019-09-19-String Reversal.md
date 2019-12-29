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
	str.split('').reduce((reversed, character) => {
	return character + reversed;
	},'');

~~~
___

First we will turn this str parameter into an array with split(''). And we setup the reduce helper functions. Reduce takes two parameters one above and one at the end where we initialize '' empty string. Esetually second parameter will be starting initial value for the function