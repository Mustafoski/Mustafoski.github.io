---
layout: post
title: "AreSimilar"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-05-06T15:39:55-04:00
modified: 2021-05-06T15:39:55-04:00
---


## AreSimilar 
Two arrays are called similar if one can be obtained from another by swapping at most one pair of elements in one of the arrays. 
___

> ##For Example
console.log(AreSimilar([1,2,3],[1,2,3])) true
console.log(AreSimilar([1,2,3],[2,1,3])) true
console.log(AreSimilar([1,2,2],[2,1,1])) false

##
<br>


~~~
function AreSimilar(a, b) {
  const c = [];
  let d = [];

  if (a.toString() === b.toString()) {
    return true;
  }

  for (let i = 0; i < a.length;i++){
    if (a[i] !== b[i]) {
      c.push(a[i]);
      d.push(b[i]);
    }
  }

  d = d.reverse();
  if (c.length === 2 && (c.toString() === d.toString())) {
    return true;
  }
  return false;
}

console.log(AreSimilar([1,2,3],[1,2,3]))
console.log(AreSimilar([1,2,3],[2,1,3]))
console.log(AreSimilar([1,2,2],[2,1,1]))
~~~

