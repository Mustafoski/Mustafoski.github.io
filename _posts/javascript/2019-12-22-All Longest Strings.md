---
layout: post
title: "All Longest Strings"
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

## All Longest Strings

 Given an array of strings we look for the string with the most characters inside. They can be one , two etc...
___

> ##For Example
For  inputArray = ['aaa','ss','bbb','a'] the output should be ['aaa','bbb']<br>

Should return true<br>
##
<br>

___


~~~
let inputArray = ['aaa','ss','bbb','a']

function allLongestStrings(inputArray){
  let longestLength = 0;
  const longestWords = [];
  
  
  inputArray.forEach(word => {
    longestLength = longestLength < word.length ? word.length : longestLength;
    
  })
  
  inputArray.forEach(word => {
    if(word.length === longestLength){
      longestWords.push(word)
    }
  })
  
  return longestWords;
}

console.log(allLongestStrings(inputArray))

~~~

___

1. We create function with parameter of n and above variable n that contains array of integer numbers;
2. We create variable largestProduct to hold the largest product and we start with index 0 n[0] * n[1] index 1;
3.We create for loop for the other values in that array not only 0 and 1 index but since we started with 0 index we start the loop with 1 e.g. i=1 then we loop until the last number but last number like in the example above 3 * nothing will give us NaN. So in the condition of for loop we do i < n.length - 1
4.Then we use largestProduct to check if is smaller than product if so product is answer else largestProduct
5. We return the largest product