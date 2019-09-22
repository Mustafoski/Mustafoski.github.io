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
date: 2017-03-01T15:39:55-04:00
modified: 2017-03-01T15:39:55-04:00
---

Longest Word

~~~ 
findLongestWord(str) {
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
