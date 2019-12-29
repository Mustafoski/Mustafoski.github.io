---
layout: post
title: "Background Color Generator"
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

## Background Color Generator


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

First we will turn this str parameter into an array with split(''). And we setup the reduce helper functions.(()=> {
	
}, '')