---
layout: post
title: "Longest Word"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2019-09-22T15:39:55-04:00
modified: 2019-09-22T15:39:55-04:00
---

Longest Word






Exercise find the longest word:
<br>
<br>Mustafoski Emir
<br>Java Spring
<br>JavaScript React
<br>SQL Posgres
Mustafoski has 10 letters and Emir has only 4


~~~ 
function findLongestWord(str) {
	let words = str.split(' ');
	let maxLength = 0;
	for(let i = 0; i<words.length;i++) {
		if(words[i].length > maxLength) {
			maxLength = words[i].length;
		}
	}
	return maxLength;
}

console.log(findLongestWord('Emir Mustafoski')) // 10
~~~

___

function findLongestWord(str) {
First we create a function and a parameter to check results.
<br>
let words = str.split(' ');
we create variable placeholder in this case (let = words) for what comes from the parameter and we split it but not spliting as an array Hint: str.split('').It is splitting into full words, in the example (Java Spring) it is splitting into ['Java', 'Spring']. If it was  without space between quotes like str.split('') it would split the word into ['J','A','V','A',' ','S','P','R','I','N','G' ]

<br>
	We create a temporary variable let maxLength and assign to 0 so we can check if it the word is bigger than maxLength.
<br>
	We create for loop to loop into the the words variable that we contain array of elements and then we check if the word of *i* from certain iteration is bigger than maxLength we assign that word to maxLength.
<br>
At the end from checking the loop for the bigger number and assigned into the temporary variable we return maxLength.


