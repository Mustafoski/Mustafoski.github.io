---
layout: post
title: "Integer Reversal"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-12-13T15:39:55-04:00
modified: 2021-12-13T15:39:55-04:00
---

## Integer Reversal

Given an Integer, return an integer that is the reverse ordering of numbers.



##For Example
console.log(reverseInt(10)) => 1 <br>
console.log(reverseInt(24)) => 42 <br>
<br>




~~~
function reverseInt(n) {
	const reversed = n
		.toString()
		.split('')
		.reverse()
		.join('');

		if(n < 0 ) {
			return parseInt(reversed) * -1;
		}
		return parseInt(reversed);
}

~~~

___
We create a function reverseInt(n) parameter *n*. 
<br>
We create a variable *reversed* and on that variable we chain couple of build in JavaScript methods on the parameter *n*
<br>
n.toString() This method toString() turns every value to string we need to turn to string so that after we can turn into an array.
<br>
After toString().split('') we chain .split('') without space between the quotes so the string will be converted into an array of single items.
<br>
toString().split('').reverse() we chain .reverse() method to reverse the order of the items of the newly created array.
<br>
toString().split('').reverse().join('') in the end we join the reversed order of items into string with .join('') method with quotes inside join.
<br>
But if the value of *n* is negative number for example -5 will be reversed to 5- which we don't want that so we check with if condition *n* < 0 and if true we parseInt the *reversed* variable and multiply with -1 to get positive number.
<br>
In the end we return parsedInt again *reversed* variable 
