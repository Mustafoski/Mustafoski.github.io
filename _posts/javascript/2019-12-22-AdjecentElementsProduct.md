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

#Adjecent Element Product
<br>
 Given an array of integers, find the pair of adjacent elements that has the largest product and return that product.


**Example**
For  n = [3,6,-2,-5,7,3] the output should be 7 * 3 =  return 21<br>

Should return true<br>
##
<br>




~~~
let inputArray = [3,6,-2,-5,7,3]

function adjacentElementsProduct(inputArray){
  let largestProduct= inputArray[0] * inputArray[1];
  
  for(let i = 1;i<inputArray.length -1 ;i++ ){
    const product = inputArray[i] * inputArray[i+1];
    
    largestProduct = largestProduct < product ? product : largestProduct
  }
  
  return largestProduct
}

console.log(adjacentElementsProduct(inputArray))

~~~

___

We create function called adjacentElementsProduct with parameter **inputArray** and local variable **largestProduct** that is equal to **inputArray** = **inputArray[0] * **inputArray**c
<br><br>
Then we create for loop that starts at 1 is less than **inputArray**.lenght - 1 and i++
And inside we create variable **product** that is equal to **inputArray[i] * inputArray[i + 1];**
<br><br>
Then we use **largestProduct = largestProduct < product ? product : largestProduct
This means if the largest number is less than product return product else return lastproduct
<br><br>
In the end we **return largestProduct**