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
		words.push(word[0].toUpperCase() + word.slice(1))
	}

	return words.join(' ')
}
~~~
___

<br><br>
First we create function capitalize with parameter *str* and create variable *words* initialized as empty array.
<br><br>
We create a for of loop where we split with space between quotes like this for(let word of str.split(" "))
<br><br>
Next we will take first character of each word so word at 0 and we will use toUpperCase() JavaScript method for capitalize letter or word.
<br><br>
Then we will join it with the rest of the word and we can get the rest of the word minus that first <b>character<b> by using the slice function
<br><br>
So we say word.slice(1) which means give me everything from the element at index 1 (second element) to the last character in the word
<br><br>
So we will join these two functions together and we will push the result into our *words* array
<br><br>
Together will look words.push(word[0].toUpperCase() + word.slice(1))
<br><br>
Then finally at the bottom after we have iterated through all these different words we will take that *words* array we will use another JavaScript method .join(' ') with a space and we will return the result