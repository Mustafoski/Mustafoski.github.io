---
layout: post
title: "Default Argument"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2023-02-12T15:39:55-04:00
modified: 2023-02-12T15:39:55-04:00
---

Default Argument
<br><br>

Double function with a parameter numberOfTimes means that a function is passed as an argument to the number of times it will be invoked that parameter numberOfTimes
**Example**<br>
console.log(double(10)) => we don’t have to give another parameter because it is 1 per default.
<br>
Solution: 20
<br>
console.log(double(10,2)) => 40
<br>

~~~
let double = (x, numberOfTimes = 1) => {
  let result = x;
  
  for (let _ of new Array(numberOfTimes).fill()) {
    result *= 2;
  }
  
  return result;
}

console.log(double(10))
~~~



We have a function called ***double*** with parameters *x* and *numberOfTimes* and local variable *result* = *x* .<br><br>

Then we iterate using for of loop with instanciating  new Array(*numberOfTimes*).fill()) 
and the variable *result* *= 2;
<br><br>
In the end we ***return result***
