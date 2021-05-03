---
layout: post
title: "AlphabeticSubSequence"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-05-03T15:39:55-04:00
modified: 2021-05-03T15:39:55-04:00
---


## AlphabeticSubSequence
Given two strings, find if first string is a subsequence of second
___

> ##For Example
console.log(AlphabeticSubSequence('zab')); Set { 122, 97, 98 }  false
console.log(AlphabeticSubSequence('effg'));Set { 101, 102, 103 } false
console.log(AlphabeticSubSequence('cdce'));Set { 99, 100, 101 } false
console.log(AlphabeticSubSequence('ace'));Set { 97, 99, 101 } true
console.log(AlphabeticSubSequence('bxz'));Set { 98, 120, 122 } true

##
<br>


~~~
function AlphabeticSubSequence(s) {
  const chars = s.split('');
  const charValues = [];

  chars.forEach((char) => {
    charValues.push(char.charCodeAt(0))
  });

  console.log(new Set(charValues))
  if (new Set(charValues).size !== charValues.length){
    return false;
  }

  for (let i =0 ; i< charValues.length -1 ; i++ ) {
    if (charValues[i] >= charValues[i+1]){
      return false;
    }
  }

  return true;
}

console.log(AlphabeticSubSequence('zab'));
console.log(AlphabeticSubSequence('effg'));
console.log(AlphabeticSubSequence('cdce'));
console.log(AlphabeticSubSequence('ace'));
console.log(AlphabeticSubSequence('bxz'));
~~~

