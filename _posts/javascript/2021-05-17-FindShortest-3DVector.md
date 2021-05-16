---
layout: post
title: "Find Shortest 3D Vector"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-05-17T15:39:55-04:00
modified: 2021-05-17T15:39:55-04:00
---

## Find Shortest 3D Vector

Finding A shortest 3D Vector 

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

function getLengthMap(vectors) {
  var lengthMapArray = [];
  for (let i = 0; i < vectors.length; i++) {
    let lengthMap = {};
    lengthMap.length = findLength(vectors[i]);
    lengthMap.index = i;
    lengthMapArray.push(lengthMap);
    console.log(lengthMapArray);
  }
  return lengthMapArray;
}

function findShortest(vectors) {
  var lengthMap = getLengthMap(vectors);
  lengthMap.sort((a, b) => a.length - b.length);
  return vectors[lengthMap[0].index];
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
We create another helper function getLengthMap(vectors) {<br>
  var lengthMapArray = [];<br>
  for (let i = 0; i < vectors.length; i++) {<br>
    let lengthMap = {};<br>
    lengthMap.length = findLength(vectors[i]);<br>
    lengthMap.index = i;<br>
    lengthMapArray.push(lengthMap);<br>
    console.log(lengthMapArray);<br>
  }<br>
  return lengthMapArray;<br>
}<br>

So we create a temporary array lengthMapArray as empty, Then we loop over the vectors.<br>
Inside the loop we create new empty object and we add properties length and index
length property is initialized with findLength(vectors[i]) in other terms length property is the return square root of vectors.<br>
index property is initialized to i to keep track of the vectors.<br>
We push the whole iteration of lengthMap object to lengthMapArray and we return the lengthMapArray<br>


In the end we create function findShortest(vectors) {<br>
  var lengthMap = getLengthMap(vectors);<br>
  lengthMap.sort((a, b) => a.length - b.length);<br>
  return vectors[lengthMap[0].index];<br>
}<br>
Where we create variable lengthMap and initialize to getLengthMap function with parameter of vectors.Then we sort the lengthMap using another JavaScript build in function sort() <br>
And we sort by using the length of the object from lengthMap object created in the previews helper function then we return the vectors with the smallest length and its its index.