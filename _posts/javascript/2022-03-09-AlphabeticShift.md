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
date: 2022-03-10T15:39:55-04:00
modified: 2022-03-10T15:39:55-04:00
---

Alphabetic Shift
<br>
Given a string, replace each its character by the next one in the English alphabet (z would be replaced by a).


**Example**<br>
- For inputString = "crazy", the output should be
alphabeticShift(inputString) = "dsbaz".<br>
0




~~~
function alphabeticShift(inputString) {
  const alphabet =  ['a', 'b' ,'c' ,'d', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n' ,'o' ,'p', 'q' ,'r' ,'s' ,'t' ,'u' ,'v' ,'w' ,'x' ,'y', 'z'];

  let inputShifted = inputString.split('');
  for(let i = 0; i< inputShifted.length;i++){
    let index = 0;

    if (inputShifted[i] !== 'z') {
      index = alphabet.indexOf(inputShifted[i]) + 1;
    }
    inputShifted[i] = alphabet[index]
  }
    return inputShifted.join('')
  }



console.log(alphabeticShift('crazy')); 4sbbaz

~~~



We create function called alphabeticShift with parameter **inputString** and local variable ***inputShifted** that is equal to **inputString.split('')** and **alphabet = ['a', 'b' ,'c' ,'d', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n' ,'o' ,'p', 'q' ,'r' ,'s' ,'t' ,'u' ,'v' ,'w' ,'x' ,'y', 'z'];**

<br><br>
We loop through the **InputShifted**  with for loop and decalare variable **index = 0** other than that I check with if statement if **inputShifted[i] !== 'z'** then **index = alphabet.indexOf(inputShifted[i]) + 1**
<br><br>
Else we **inputShifted[i] = alphabet[index]**
<br><br>
\
In the end we **inputShifted.join('')**