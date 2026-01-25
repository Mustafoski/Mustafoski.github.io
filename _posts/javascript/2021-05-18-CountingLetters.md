---
layout: post
title: "CountLetters"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-05-18T15:39:55-04:00
modified: 2021-05-18T15:39:55-04:00
---

## CountLetters

Counting letters from string
___

> ##For Example
console.log(countLetters('ffffeerttttooo')) 4f,2e,1r,4t,3o
##
<br>

___


~~~
function countLetters(str) {
  let tempArray = str.split('');
  let letters = [];
  let count = 1;

  for (let i = 0;i<tempArray.length;i++) {
    if (tempArray[i] === tempArray[i+1]){
      count++
    }
    else {
      let value = `${count}${tempArray[i]}`;
      letters = [...letters,value]
      count = 1;
    }
  }
  
  return letters.join();
}

console.log(countLetters('ffffeerttttooo'))



~~~

___

First we create a *function countLetters(str) {* with the string as a parameter. 
Then we split the string into an array with the split JavaScript build in function that transforms string into an array. <br>
We create empty array called letters and we create a counter called *count* and we initialize to 1.
<br>
We create for loop to loop through the array we created with spliting the string str and we check
*if (tempArray[i] === tempArray[i+1])* so we check if the current string is equal to the next string we increase the count with *count++* <br>
else {<br>
      let value = `${count}${tempArray[i]}`;<br>
      letters = [...letters,value]<br>
      count = 1;<br>
    }<br>
  }<br>
  <br>
  return letters.join();
}<br>
And in the else statement we create a value variable that holds the count and the string <br>
letters array we push with spread operator to the new letters and its new values<br>
and every time we have new value we start the counter to 1;
<br>
At the end we return letters array with join() build in JavaScript function that joins the array into string/ or it converts into string.