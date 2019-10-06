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
date: 2019-10-06T15:39:55-04:00
modified: 2019-10-06T15:39:55-04:00
---

## Integer Reversal

Given an Integer, return an integer that is the reverse ordering of numbers.

___

> ##For Example
reverseInt(12) = 21 <br>
reverseInt(876) = 678<br>
reverseInt(250) = 52<br>
reverseInt(-15) =51-<br>
Should return true<br>
##
<br>

___


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

1. We take the parameter and somehow treat it like a string 
2. We will split that number, reverse and join
3. Then we should take care of the examples like "51-" this will continue to be string so we need to parse it to Integer with parseInt method.
4. If we have number e.g. -5 we need to maintain the sign.
