---
layout: post
title: "Sentence Capitalization-v1"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-12-29T15:39:55-04:00
modified: 2021-12-29T15:39:55-04:00
---

## Sentence Capitalization v1

<br>

Write a function that accepts a string. The function should capitalize the first letter of each word in the string then return the capitalized string.

<br>
Examples <br>
capitalize('a short sentence') => return 'A Short Sentence<br>
capitalize('a lazy fox') => return 'A Lazy Fox'<br>
capitalize('look, it is working!') => return 'Look, It Is Working'<br>
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

<br><br>
First we create function anagrams with parameters *stringA* and *stringB*.
<br><br>
Then we create helper function cleanString with parameter *str* and we return *str*.replace which is build in JavaScript method. replace will strip out any spaces or any punctuation and turn into lowercase with chaining the toLowerCase();
<br><br>
Than we chain .split('') method to turn the string *str* into array
<br><br>
Then we chain .sort() method to sort alphabetically the characters from the array done with split method
<br><br>
In the end we join the characters from the array, sorted with sort method and now joined with .join('') method. All these functions are build in JavaScript helpers
<br><br>
From the cleanString function all these tasks done above are returned
<br><br>
In the main function anagrams we return cleanString(*stringA*) === cleanString(*stringB*) and if it is true it is anagram.