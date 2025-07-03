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
date: 2021-12-26T15:39:55-04:00
modified: 2021-12-26T15:39:55-04:00
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


~~~
___

First we create function in our case steps with only one parameter named *n* ( n is the number of rows as described in the example above) and *row* and we will default the *row* to 0, third argument is *stair* we initial with empty string;
<br><br>
We check if (*n* === *row*) and if *row* we return; 
<br><br>
Next we check if (*n* === stair.length) we console.log(stair)
<br><br>
Inside the if statement we recursivly use steps(*n* ,*row* + 1)
<br><br>
If we meet the above case we don't need to do anything else so we make sure that we use the word ***return*** before the steps(*n* ,*row* + 1)
<br><br>
The last thing we have to do is handle the case in which we are still assembling our *stair* string and if the length of the *stair* is less than or equal to the row that we are currently working on we are going to add a '#' otherwise empty space;
<br><br>
We check with if statement if(stair.length <= row) we return *stair* += '#' else *stair* += ' ';
<br><br>
Then we again we use recursion calling steps(*n*, *row*, *stair*)
<br><br>
