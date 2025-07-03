---
layout: post
title: "Alternating Sum"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-03-12T15:39:55-04:00
modified: 2022-03-12T15:39:55-04:00
---

Alternating Sum
<br><br>
You are given an array of positive integers - the weights of the people. Return an array of two integers, where the first element is the total weight of team 1, and the second element is the total weight of team 2 after the division is complete.


**Example**<br>
console.log(alternatingSums([50, 60, 60, 45, 70])) [180, 105] <br>
even: 60 + 60 + 50 = 170 <br> 
odd: 45 + 70 = 105 <br>
- 




~~~
function alternatingSums(a) {
  let evenSum = 0;
  let oddSum = 0;

  a.forEach((element,index) => {
    if (index % 2 === 0) {
      evenSum += element;
    }else {
      oddSum += element
    }
  })

  return [evenSum,oddSum]
}

console.log(alternatingSums([50, 60, 60, 45, 70])) [180, 105]

~~~



We create function called alternatingSums with parameter **a** and local variable **evenSum = 0**  and **oddSum = 0**
<br><br>
We loop the array given into the parameter *a* with forEach loop that takes arguments *element* and *index* 
<br><br>
Inside the forEach loop we check if *index* % 2 === 0 than we **eventSum += element** else **oddSum += element**
<br><br>
*The forEach() method executes a provided function once for each array element.* - **MDN**
<br><br>
So if all the cases above are false we **return [eventSum, oddSum**