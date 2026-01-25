---
layout: post
title: "Truncate String"
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

## Truncate String

 If the length of the string is less than or equal to the given number, just return the string without truncating it. Otherwise, truncate the string. Meaning keep the beginning of the string up until the given number and discard the rest.Also we have 3 positions if avaible for the 3 dots ...; If we have number bigger than the string we dont use dots.

___

> ##For Example
let string = 'Orange'
let num1 = 1
let num2 = 3
let num3 = 9 
Should return true<br>
##
<br>

___


~~~
function truncateString(str, num) {
	
	if(str.length > num  && num > 3){
		return str.slice(0,(num-3)) + '...'
	}
	else if(str.length > num && num <= 3) {
		return str.slice(0, num) + '...';
	}
	else {
		return str;
	}
}
console.log(truncateString(string,num1)); // "0..."
console.log(truncateString(string,num2)); // "0ra..."
console.log(truncateString(string,num3)); // "0range"

~~~

___

1. In the first if statement str.length = 6 > 3 and 1 > 3 its false so we return str.slice(0,(num-3))+ '...' so we return only the first 0 index e.g. "O..."

2. In the second if statement 6 > 3 and 3 <=3 so we return str.slice(0,3)+ ... so the return is from 0 index - 3th index "Ora..."

3. Last case num is 9 its bigger than 6 (Letters of Orange) so we return full without dots "Orange"


