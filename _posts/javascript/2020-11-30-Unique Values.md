---
layout: post
title: "Unique Values-v3"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2020-11-30T15:39:55-04:00
modified: 2020-11-30T15:39:55-04:00
---

## Unique Values-v3

Unique Values is when in a string every letter is unique if they are all different unique then it is true of not like the second example if there are duplicates than it is false
___

> ##For Example<br>
  abcde => true<br>
 abcda => false<br>
>
##
<br>

___

~~~

function unique(str) {
  return new Set(str).size === str.length;
}




~~~

function unique(str){ <br><br>

First we create a function called unique and pass an argument string called str.

<br><br>
  return new Set(str).size === str.length;

<br><br>
We return new Set that has an argument str if that will be equal to str.
We check if Set(str).size (Note: We set we use size instead of length) and if that return is equal to str.length we eather return true or false;



