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

All Longest Strings

 Given an array of strings we look for the string with the most characters inside. They can be one , two etc...


**Example**<br>
For  inputArray = ['aaa','ss','bbb','a'] => ['aaa','bbb']<br>






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

console.log(allLongestStrings(inputArray))  ['aaa','bbb']

~~~

First we create a function called allLongestStrings with parameter **inputArray** and two variables **longestLenght = 0** and **longestWords = []**
<br><br>
We are going to iterate through each one with forEach loop from **inputArray** and callback function with parameter *word* and we check **longestLength = longestLength < *word.length* ? *word.length* : **longestLength**<br>
This reads check if longestLength is less than word.length and if it is less return word.length else return longestLength. 
<br><br>
We are going to iterate again through each one with forEach loop from **inputArray** and callback function with parameter *word* and we check if *word.lenght* === **longestLength** we push to the **longestWords.push(*word*)**
<br><br>
In the end we **return longestWords**