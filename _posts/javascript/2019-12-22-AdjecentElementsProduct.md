---
layout: post
title: "Adjecent Element Product"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2019-12-22T15:39:55-04:00
modified: 2019-12-22T15:39:55-04:00
---

## Adjecent Element Product

 Given an array of integers, find the pair of adjacent elements that has the largest product and return that product.
___

> ##For Example
For  n = [3,6,-2,-5,7,3] the output should be 7 * 3 =  return 21<br>

Should return true<br>
##
<br>

___


~~~
let n = [3,6,-2,-5,7,3]

function adjacentElementsProduct(n){
  let largestProduct= n[0] * n[1];
  
  for(let i = 1;i<n.length -1 ;i++ ){
    const product = n[i] * n[i+1];
    
    largestProduct = largestProduct < product ? product : largestProduct
  }
  
  return largestProduct
}

console.log(adjacentElementsProduct(n))

~~~

___

1. We create function with parameter of n and above variable n that contains array of integer numbers;
2. We create variable largestProduct to hold the largest product and we start with index 0 n[0] * n[1] index 1;
3.We create for loop for the other values in that array not only 0 and 1 index but since we started with 0 index we start the loop with 1 e.g. i=1 then we loop until the last number but last number like in the example above 3 * nothing will give us NaN. So in the condition of for loop we do i < n.length - 1

4. Then we use largestProduct to check if is smaller than product if so product is answer else largestProduct
5. We return the largest product