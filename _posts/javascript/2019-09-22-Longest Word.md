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

Longest Word<br>


Mustafoski has 10 letters and Emir has only 4

Find the longest word


Exercise find the longest word:
<br>
<br>Mustafoski Emir
<br>Java Spring
<br>JavaScript React
<br>SQL Posgres

First we create a function and a parameter to check results.
we create variable placeholder for what comes from the parameter and we split it but not spliting as an array Hint: str.split('').
<br>
We split it like this str.split(' ') with the space between so that the example above will be resulting as:
Mustafoski Emir
Mustafoski and Emir
<br>
Then we check if the splited results are larger than 0 or in this case maxLength. if it is larger than 0 we send the results to maxLength and we return maxLength.


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



Hint: For full word you split with space inside.
