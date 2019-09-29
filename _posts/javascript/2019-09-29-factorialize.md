---
layout: post
title: "Factirialize"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2019-09-29T15:39:55-04:00
modified: 2019-09-29T15:39:55-04:00
---

## Factirialize

<br>

 So basically, factorializing numbers makes it easier to figure out the number of combinations which is useful when calculating probabilities or statistics. ... If the integer is represented with the letter n, a factorial is the product of all positive integers less than or equal to n.
 Example 5!, 10!, 25!

 <br>

 function factorialize(num) {
 	let result = 1;
 	for(let i = num; i>0; i--){
 	result *= i;
 }
 return result;
}

console.log(factorialize(5)) => 120
console.log(factorialize(10)) => 3628800

We create variable <strong>result</strong> and initialize to 1;
<br>
Then we will create a loop where we create variable i = num, then i will always be greater than 0 and i will be deducted by one on each loop;
<br>
Then <strong>result</strong> will be result = result * i; 
or shorthand result * = result * i
<br>
In the end we return result
