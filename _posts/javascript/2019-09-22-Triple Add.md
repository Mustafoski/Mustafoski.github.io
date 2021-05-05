---
layout: post
title: "Triple Add"
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

Triple Add

tripleAdd(10)(20)(30);
<br>
// returns the total of 3 numbers/ invokations


~~~
function tripleAdd(num1) {
	return function(num2) {
		return function(num3) {
			return num1 + num2 + num3;
		};
	};
}
tripleAdd(10)(20)(30);
~~~

First we need to know is that we don't invoke 3 functions but one function called tripleAdd and we invoke the returns inside tripleAdd.N
<br>
So we define a function tripleAdd and it will take our first number as parameter in our case num1.
Inside a tripleAdd all we want to do is to return another function and this function will take our second number num2 as a parameter. 
<br>
Inside the second function we return a third function and this function will take third number as a parameter in our case num3.
<br>
Finally we return num1+num2+num3.
So we have a function that returns a function and that function returns third function and in the end we add all the function parameters