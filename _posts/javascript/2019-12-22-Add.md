---
layout: post
title: "Adding array of numbers"
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

## Adding array of numbers

Given an array we add them using ES6 spread operator

___

> ##For Example
For a = [1,2,3,4,5] the output should be 15<br>
For a = [2,3] the output shoud be 5<br>
Should return true<br>
##
<br>

___


~~~
let x  = [1,2,3,4,5];  
let x1  = [2,3]; 


function add(x) {
	let total = 0;
	x.forEach(num =>  {
		total += num
	});

	return total;

} 
add(x) =>15
add(x1) => 5

~~~

___

1. First we create example arrays e.g. x and x1;
2. We create variable total to 0.
3. The parameter x we loop with forEach loop where we give parameter (num). so for each num in the x array add to the total variable created earlier.
4.Lastly we return the total