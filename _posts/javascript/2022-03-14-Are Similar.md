---
layout: post
title: "Are Similar"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-03-14T15:39:55-04:00
modified: 2022-03-14T15:39:55-04:00
---

Are Similar
<br><br>
Two arrays are called similar if one can be obtained from another by swapping at most one pair of elements in one of the arrays.

Given two arrays a and b, check whether they are similar.

**Example**<br>
console.log(areSimilar([1, 2, 3], [1, 2, 3])); true<br>
console.log(areSimilar([1, 2, 3], [2, 1, 3])); true<br>
console.log(areSimilar([1, 2, 2], [2, 1, 1])); false<br>




~~~
function areSimilar(a, b) {
  const c = [];
  let d = [];
  
  if (a.toString() === b.toString()){
    return true;
  }

  for(let i = 0;i<a.length;i++){
    if (a[i] !== b[i]) {
      c.push(a[i])
      d.push(b[i])
    }
  }
  d = d.reverse();
  if (c.length === 2 && (c.toString() === d.toString())){
    return true;
  }
  return false;

}

console.log(areSimilar([1, 2, 3], [1, 2, 3])); true
console.log(areSimilar([1, 2, 3], [2, 1, 3])); true
console.log(areSimilar([1, 2, 2], [2, 1, 1])); false


~~~



We create function called areSimilar with parameters *a*, *b* and variables *c = []* and *d = []*
<br><br>
If are converting parameters *a* and *b* to string with toString() and if they are are true we **return true** <br> The toString() method returns a string representing the object. -MDN
<br><br>
We iterate trough array *a* and we check if **a[i] !== b[i]** we use the push method and we push them into variable arrays *c* and *d*
<br><br>
After that we reverse the *d* array with reverse method and check if **c.length === 2 && (c.toString() === d.toString())** we **return true** otherwise we **return false**
<br><br>
The reverse() method reverses an array in place. The first array element becomes the last, and the last array element becomes the first. -MDN

