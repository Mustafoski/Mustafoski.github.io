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

First we create function in our case steps with only one parameter named n ( n is the number of rows as described in the example above)
<br>
We create a loop with let row = 0 (starting at 0); row < n and row ++
We create also temporary variable called stair and initialize to an empty string;
<br>
inside the loop we create another loop for the columns so we create column variable to start at 0 to be less than n and to increment by 1 every iteration.
<br>
Now we check if (column <=  row) and if it is true stairs will concatenate with '#' otherwise stairs remains the same.
For example if *n* is 3

first loop row is 1 and in the second loop column is 1 so in our if statement we have If column is less or equal to row that it is true. This condition passes and we have one stairs '#'

Second loop row is 2 and column is also 2 again the if condition passes but since stairs is now '#' we concatenate like this stairs = stairs + '#' so stairs from first loop is '#' than this statement is 
stairs = '#' + '#' which makes stairs => '##'

Third and final loop again row is 3 column is 3 the if condition passes and now we have stairs of '###'

Since we initialize n to be 3 row and column loop fails and that bring us to the end.

In the end we just console.log the stairs