---
layout: post
title: "Add Border"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2019-12-29T15:39:55-04:00
modified: 2019-12-29T15:39:55-04:00
---

## Add Border

Outside of the values we give border with the style of *

___

> ##For Example
For n = 29 the output should be 2+9 =  return 11<br>

Should return true<br>
##
<br>

___


~~~
let n = 29;

function addTwoDigits(n){
  const nums = n.toString().split('');
  
  return nums.reduce((x, y) => {
    return parseInt(x)+ parseInt(y)
  })
}

console.log(addTwoDigits(n))

~~~

___

1. We create a function with parameter n;
2. We create variable nums to hold the single index where n is turned to String and splited into chunks.
3. We return nums with reduce function where as parameters we use x and y (still strings...) and again we return but we parse x and y into numbers with parseInt.
4. Lastly we add them together