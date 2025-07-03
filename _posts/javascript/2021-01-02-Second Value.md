---
layout: post
title: "Second Value"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-01-02T15:39:55-04:00
modified: 2021-01-02T15:39:55-04:00
---

## Second Value
Second Value is when we return the middle value and unique values.

___

> ##For Example<br>
  [1] => 1<br>
  [3,2,88,3,-11,67,7] => [-11,2,3,7,67,88]<br>
>
##
<br>


___

~~~

function secondValue(arr) {
	let values = [...new Set(arr)].sort((a,b) => a - b);
	if(values.length < 2) {
		return values
	}
}



~~~

function secondValue(arr){ <br><br>

First we create a function called secondValue and pass an argument called arr.

<br><br>

let values = [...new Set(arr)];
<br><br>

We create variable values and we use Set data structure to eliminate the doubles 

<br><br>
	let values = [...new Set(arr)].sort((a,b) => a - b);


<br><br> 

We attach the sort method to sort in ascending order
<br><br> 