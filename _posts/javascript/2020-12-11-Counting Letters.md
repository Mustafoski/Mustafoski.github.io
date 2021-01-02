---
layout: post
title: "Counting Letters"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2020-12-10T15:39:55-04:00
modified: 2020-12-10T15:39:55-04:00
---

## Counting Letters

Counting Letters is when you count the letters of each one in the sentence and return the one with the most different letters.
___

> ##For Example<br>
 javascript is a great language=> javascript <br>

>
##
<br>

___

~~~



function countingLetters(str) {
  let tempArr = str.split(" ");
  tempArr = tempArr.map(item => {
    let tempItem = item.toLowerCase().split('');
    return tempItem.reduce((acc,curr) => {
      acc[curr] = acc[curr] ? acc[curr] +1: 1;
      if(acc[curr] > acc.max) {
        acc.max = acc[curr]
      }
      return acc;
    },{max:1,word:item})
  })

  let amount = 1;
  let word = '';
  for (const item of tempArr) {
    if (item.max > amount) {
      amount = item.max;
      word = item.word
    }
  }
  if(amount > 1) {
    return word
  }
  return -1;
}

console.log(countingLetters("javascript is a great language"));]


~~~

