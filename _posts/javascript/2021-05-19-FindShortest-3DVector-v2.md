---
layout: post
title: "Find Shortest 3D Vector-v2"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-05-18T15:39:55-04:00
modified: 2021-05-18T15:39:55-04:00
---

## Find Shortest 3D Vector v2

Finding A shortest 3D Vector  v2

___

> ##For Example
For example, for the array of 3D vectors [ [1,1,1], [2, 2, 2], [3, 3, 3]] findShortest
should return the first vector (array[1,1,1]) because it is the shortest 
##
<br>

___


~~~
function findLength(vector) {
  var x = Math.pow(vector[0], 2);
  var y = Math.pow(vector[1], 2);
  var z = Math.pow(vector[2], 2);
  return Math.sqrt(x + y + z);
}

function findShortest2(vectors) {
  return vectors.reduce((a, b) => (findLength(a) < findLength(b)) ? a : b);
}


var vectors = [
  [1, 1, 1],
  [2, 2, 2],
  [3, 3, 3],
];

var shortest = findShortest(vectors);
console.log(shortest); [1,1,1]



~~~

___

In order to solve the Find Shortest 3D Vector we first create a helper function in our case *function findLength(vector)*
We have helper function for the formula which is x^2 + y^2 + z^2 squared. We have javascript functions Math.pow that takes the first vector in our case *vector[o],2* and second argument is how much to the power of. And at the end we return another JavaScript build in function Math.sqrt for finding the square root of number or numbers in our case  <br>
*Math.sqrt(x + y + z);*
<br>
Then we write another functional function build in JavaScript called reduce<br>
*function findShortest(vectors) {<br>
  return vectors.reduce((a, b) => (findLength(a) < findLength(b)) ? a : b);<br>
}*<br>
We return the vectors.reduce of a and b where we call findLength helper function to a and to b.
If a is lesser than b we return a else b.