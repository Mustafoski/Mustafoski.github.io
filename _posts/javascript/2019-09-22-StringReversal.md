---
layout: post
title: "String Reversal"
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

## String Reversal


Example:<br>
reverse('apple') = 'leppa'<br>
reverse('hello') = 'olleh'<br>
reverse('Greetings') = 'sgniteerG'<br>

~~~
function reverse(str){
	const arr = str.split('');
	arr.reverse();
	return arr.join('');
}
~~~

We create a function in our case called reverse with a parameter I choose *str* 
JavaScript have many String Helper Methods that we can use to make our development easier and we will use some of them.
<br>
We create a const arr to hold the value that it will passed into the parameter *str* and we split the value into array. 
<br>
This will look like this if *str* = apple it will split into ['a','p','p','l','e'];
<br>
Then we use the String Helper Method reverse() to the arr constant to reverse the array into 
['e','l','p','p','a'];
<br>
At the end we must return some value and we return the arr reversed and we chain another String Helper Method join('') which will join the array into full variable String (not an array ) in our case it will join the arr into 'leppa'
