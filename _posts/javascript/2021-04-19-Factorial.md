---
layout: post
title: "Factorial v2"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-19-04T15:39:55-04:00
modified: 2021-19-04T15:39:55-04:00
---

## Factorial v2

So basically, factorializing numbers makes it easier to figure out the number of combinations which is useful when calculating probabilities or statistics. … If the integer is represented with the letter n, a factorial is the product of all positive integers less than or equal to n. Example 5!, 10!, 25!

___

> ##For Example
test 5! === return 12o <br>
test 4! === return 24 <br>
test 1! === return 1 <br>
Should return true<br>
##
<br>

___


~~~
function factorial(num) {
	if (num === 1) {
		return num;
	}
	else {
		return num * factorial(num-1)
	}
}

console.log(factorial(4))
~~~

___



