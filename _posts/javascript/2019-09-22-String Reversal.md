---
layout: post
title: "String Reversal-v2"
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

## String Reversal


Example:<br>
reverse('apple') = 'leppa'<br>
reverse('hello') = 'olleh'<br>
reverse('Greetings') = 'sgniteerG'<br>

~~~
function reverse(str){
	const arr = str.split('');
	arr.reverse();
	return arr.join('');
}
~~~
We take the parameter str and we split into array into the array varable
Then we reverse the array and in the end we join the reversed array;

