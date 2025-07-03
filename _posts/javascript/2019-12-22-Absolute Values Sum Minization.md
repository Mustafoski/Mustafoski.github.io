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
date: 2019-12-22T15:39:55-04:00
modified: 2019-12-22T15:39:55-04:00
---

## Absolute Values Sum Minization 
<br>
Given a sorted array of integers a, find an integer x from a such that the value of 
	abc(a[0] - x) + abs(a[1] - x) + ... + abc(a[a.length - 1] - x)
is the smallest possible (here abc denotes the absolute value).
If there are several possible answers output the smallest one.


**Example**

For a = [2, 4, 7], the output should be <b>
absoluteValuesSumMinimization(a) = 4. <b>

For a = [2, 4, 7, 6], the output should be <b>
absoluteValuesSumMinimization(a) = 4. <b>

For a = [2, 4, 7, 6, 6], the output should be <b>
absoluteValuesSumMinimization(a) = 7. <b>

For a = [2, 4, 7, 6, 6, 8], the output should be <b>
absoluteValuesSumMinimization(a) = 7. <b>





~~~
function absoluteValuesSumMinimization(x) {
	const isEven = x.length % 2 === 0;

	return isEven ? x[x.length / 2 - 1] : x[Math.floor(x.length / 2)];

} 

~~~

___

1. First we check if the number is even.
2. If the number is even we take the length of the array of numbers and divide by 2 and then - 1;
3. Else if the length of the array is odd number we use the second else part where we Math.floor for full number and we divide by 2.

First we create function in our case *absoluteValuesSumMinimization* with only one parameter named **x** , and a temporary variable **isEven**
<br><br>
First we check if the number is even.<br>
**isEven = x.length % 2 === 0**<br>
<br><br>
If the number is even we take the length of the array of numbers and divide by 2 and then - 1;<br>
**return isEven ? x[x.length / 2 - 1] : x[Math.floor(x.length / 2)];**
<br><br>
