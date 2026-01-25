---
layout: post
title: "String Repeater"
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

## String Repeater

As the title suggest we take a string and we repeat by the number given by the second parameter. If second parameter is not a positive number we return an empty string.

___

> ##For Example
let str = 'candy apple'
let num = -1
let str = 'candy apple'
let num = 4 
stringRepeater(str, num) <br>
stringRepeater(str, num)<br>
Should return true<br>
##
<br>

___


~~~
function stringRepeater(str, num) {
	
	if(num > 0 ){
	return str.repeat(num)
	}
	return "";
}

~~~

___

1. First we check if num is bigger then 0 and if it is we return the string by the number provided in the second parameter.

2. As mention above if the number is negative number or as the code provided above number is not bigger than 0 we return empty string ""
