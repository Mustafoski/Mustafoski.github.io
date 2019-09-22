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

So we have a Function that is returning a Function which in turn it returns another Function that is returning our total.