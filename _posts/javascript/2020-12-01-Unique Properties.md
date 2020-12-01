---
layout: post
title: "Unique Properties"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2020-10-16T15:39:55-04:00
modified: 2020-16-15T15:39:55-04:00
---

## Unique Properties

Unique Properties is when in a string every letter is unique if they are all different unique then it is true and returns all unique values of an array if not like the second example if there are duplicates than it returns only unique values
___

> ##For Example<br>
  a,b,c,d,e => abcde<br>
 a,b,c,d,a => abcd<br>
>
##
<br>

___

~~~

let arr = [
{
	letter:"a"
},
{
	letter:"b"
},
{
	letter:"c"
},
{
	letter:"a"
}
];

function getUnique(arr){
	let tempArr = arr.map(item => item.letter);
	return [... new Set(tempArr)];
}

we return [a,b,c]


~~~

function getUnique(arr){ <br><br>

First we create a function called getUnique and pass an argument called arr.

<br><br>

let tempArr = arr.map(item => item.letter);
<br><br>

We create temporary variable array tempArr and use the map method where we map through the arr and we say whenever which and every item we would want to return the letter value into item.letters

<br><br>
	return [... new Set(tempArr)];


<br><br> 

Then for single values we use the data structure Set and we return spread operator to spread every new addition and substiction of unique data provided with new Set and inside the parathesis we put the temporary variable tempArr



