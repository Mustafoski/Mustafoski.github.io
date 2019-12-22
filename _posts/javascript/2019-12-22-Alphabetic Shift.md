---
layout: post
title: "Alphabetic Shift"
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

## Alphabetic Shift


It is a type of substitution cipher in which each letter in the plaintext is 'shifted' a certain number of places down the alphabet. For example, with a shift of 1, A would be replaced by B, B would become C, and so on.

 
___

> ##For Example
For  inputString = 'crazy' the return 'dsbaz'<br>

Should return true<br>
##
<br>

___


~~~

let inputString = 'crazy';

function alphabeticShift(inputString) {
  const alphabet = {
    'a':'b','b':'c','c':'d',
    'd':'e','e':'f','f':'g',
    'g':'h','h':'i','i':'j',
    'j':'k','k':'l','l':'m',
    'm':'n','n':'o','o':'p',
    'p':'q','q':'r','r':'s',
    's':'t','t':'u','u':'v',
    'v':'w','w':'y','y':'z',
    'z':'a'
  };
  
  let inputShifted = inputString.split('');
  for(let i = 0; i< inputShifted.length;i++) {
    inputShifted[i] = alphabet[inputShifted[i]];
  }
  return inputShifted.join('');
}

console.log(alphabeticShift(inputString))

~~~

___

1. We create Object of key/value pairs of the whole alphabet but remember 'z':'a' at the end;
2. inputShifted takes from parameter inputString splited value ( in our case 'crazy') and turn it into an array ([c,r,a,z,y])
3. We create for loop to loop through the splited word ([c,r,a,z,y])
4. inputShifted[i] is looking into alphabet and takes the from key/value we take the value
5. At the end we return the inputShifted and joined as whole string.

