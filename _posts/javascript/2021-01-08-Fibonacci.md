---
layout: post
title: "LinkedList"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-01-08T15:39:55-04:00
modified: 2021-01-08T15:39:55-04:00
---

## LinkedList
SLinkedList is data structure that is good for lists.

___

> ##For Example<br>
console.log(recursive(6));=> 8
console.log(recursive(6));=> 89
>
##
<br>


___

~~~

let recursive = function (n) {
  if (n <= 2) {
    return 1;
  } else {
    return recursive(n - 1) + recursive(n - 2);
  }
};

console.log(recursive(6));






~~~

We create name function called recursive with the value of n<br><br>

if ( n <=2 ) { return 1;}
<br><br>

if the parameter is less or equal to 2 we return 1
<br><br>

else we recurisvly return recursive(n - 1) + recursive (n - 2)

<br><br>
	
