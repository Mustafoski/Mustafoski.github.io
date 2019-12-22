---
layout: post
title: "Absolute Values Sum Minization"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2019-09-29T15:39:55-04:00
modified: 2019-09-29T15:39:55-04:00
---

## Absolute Values Sum Minization

Given a sorted array of integers a, find an integer x from a such that the value of 
	abc(a[0] - x) + abs(a[1] - x) + ... + abc(a[a.length - 1] - x)
is the smallest possible (here abc denotes the absolute value).If there are several possible answers output the smallest one.

___

> ##For Example
For a = [2,4,7] the output should be 4<br>
For a = [2,4,7,6] the output shoud be 4<br>
Should return true<br>
##
<br>

___


~~~
let x  = [2,4,7];  => 4
let x1  = [2,4,7,6]; => 4
let x2 = [2,4,7,6,6]; => 7
let x3 = [2,4,7,6,6,8] => 7

function absoluteValuesSumMinimization(x) {
	const isEven = x.length % 2 === 0;

	return isEven ? x[x.length / 2 - 1] : x[Math.floor(x.length / 2)];

} 

~~~

___

1. First we check if the number is even.
2. If the number is even we take the length of the array of numbers and divide by 2 and then - 1;
3. Else if the length of the array is odd number we use the second else part where we Math.floor for full number and we divide by 2.