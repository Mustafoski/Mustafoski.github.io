---
layout: post
title: "Factirialize"
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

## Factorial Calculator

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
function factorialize(num) { 
	let result = 1; 
	for(let i = num; i>0; i–){ 
		result *= i; 
		} 
		return result; 
	}

console.log(factorialize(5)) => 120 
console.log(factorialize(10)) => 3628800

~~~

___

1. We create variable result and initialize to 1;

2.Then we will create a loop where we create variable i = num, then i will always be greater than 0 and <strong>i</strong> will be deducted by one on each loop;

3.Then result will be result = result * i; or shorthand result * = result * i In the end we return result.
