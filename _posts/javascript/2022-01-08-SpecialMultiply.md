---
layout: post
title: "Special Multiply"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-01-08T15:39:55-04:00
modified: 2022-01-08T15:39:55-04:00
---

## Special Multiply
Special Multiply is a form of code where we have one function and we check if they are not arrays, strings or objects plain numbers and we return a callback function where we multiply the parameters;


Example:<br>
console.log(specialMultiply(3,2)) // 6 <br>
console.log(specialMultiply(5,-2))// -10 <br>





~~~
function specialMultiply(a,b){
  if(arguments.length === 1){
    return function(b){
      return a*b;
    }
  }
  return a*b;
}
console.log(specialMultiply(3,2)) // 6
console.log(specialMultiply(5,-2))// -10
~~~
___
We create a function called specialMultiply with parameter called *a* and *b* 
<br><br>
We check if (arguments.length ===1) {} 
<br><br>
If true we return another function with parameter *b* and return a*b
<br><br>
In the end we return again a*b
<br><br>
