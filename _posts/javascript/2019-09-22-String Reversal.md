---
layout: post
title: "String Reversal"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2017-03-01T15:39:55-04:00
modified: 2017-03-01T15:39:55-04:00
---

## String Reversal


Example:
reverse('apple') = 'leppa'
reverse('hello') = 'olleh'
reverse('Greetings') = 'sgniteerG'


function reverse(str){
	const arr = str.split('');
	arr.reverse();
	return arr.join('');
}

We take the parameter str and we split into array into the array varable
Then we reverse the array and in the end we join the reversed array;


#Solution 2

function reverse(str) {
	str.split('').reduce((reversed, character) => {
	return character + reversed;
	},'');
}