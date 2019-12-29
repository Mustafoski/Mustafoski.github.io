---
layout: post
title: "Sentence Capitalization"
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

## Sentence Capitalization

<br>

Write a function that accepts a string. The function should capitalize the first letter of each word in the string then return the capitalized string.

<br>
Examples <br>
capitalize('a short sentence') => return 'A Short Sentence<br>
capitalize('a lazy fox') => return 'A Lazy Fox'<br>
capitalize('look, it is working!') => return 'Look, It Is Working'
<br>

~~~
function capitalize(str){

	const words = [];
	for(let word of str.split(' ')){
		words.push(word[0].toUpperCase() + word.splice(1))
	}

	return words.join(' ')
}
~~~
___

<br>
Make an empty array words, <br>
Split the input string by spaces to get an array,<br>
For each word in the array,<br>
Uppercase the first letter of the word,<br>
Join first letter with the rest of the string<br>
Push result into words array<br>
Join words into a string and return it.<br>