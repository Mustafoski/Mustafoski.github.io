---
layout: post
title: "AlternatingSum"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-05-04T15:39:55-04:00
modified: 2021-05-04T15:39:55-04:00
---


## Alternating Sum
An alternating sum is a sequence of arithmetic operations in which each addition. is followed by a subtraction, and viceversa, applied to a sequence of numerical entities
___

> ##For Example
console.log(AlternatingSum([50,60,60,45,70])) [ 180, 105 ]

##
<br>


~~~
function AlternatingSum(x) {
  let evenSum = 0;
  let oddSum = 0;
  
  x.forEach((element,index) => {
    if (index % 2 === 0){
      evenSum += element
    } else {
      oddSum +=element;
    }
  })
  return [evenSum,oddSum]
}

console.log(AlternatingSum([50,60,60,45,70])) [ 180, 105 ]
~~~

