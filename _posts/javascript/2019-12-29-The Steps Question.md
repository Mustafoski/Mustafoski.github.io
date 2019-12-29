---
layout: post
title: "The Steps Question"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2019-12-29T15:39:55-04:00
modified: 2019-12-29T15:39:55-04:00
---

## The Steps Question


Write a function that accepts positive number N. The function should console log a step shape with N levels using the # character. Make sure the step has spaces on the right hand side.

Example:<br>
steps(2)<br>
	'# '<br>
	'##'<br>
steps(3)<br>
	'#  '<br>
	'##' <br>
	'###'<br>
steps(4)<br>
	'#    '<br>
	'##  '<br>
	'### '<br>
	'####'<br> 


~~~
function steps(n) {
	for(let row = 0; row < n; row++) {
		let stair = '';

		for(let column = 0; column < n; column++){
			if(column <= row) {
				stair += '#'
			}else {
				stair += ' '
			}
		}
		console.log(stair)
	}
}

~~~
___

From 0 to n we iterate through rows<br>
Create an empty string stair<br>
from 0 to n we iterate through columns<br>
If the current column is equal to or less than the current row<br>
Add a '#' to the stair<br>
Else<br>
add a space to the stair<br> 
console.log(stair)<br>