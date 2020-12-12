---
layout: post
title: "Reverse String v4"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2020-12-111T15:39:55-04:00
modified: 2020-12-11T15:39:55-04:00
---

## Reverse String v4

Reversed String is when we reverse a string or a word in a sentence and then return the whole string with reversed letters.
___

> ##For Example<br>
  'this is a string of words' => 'sith si a gnirts fo sdrow'<br>
  'Coding JavaScript' => 'gnidoC trircsavaJ'<br>
>
##
<br>


___

~~~


function reverse(str) {
  // check input 
  if (!str || str.length < 2 || typeof str !== 'string'){
    return 'hmm that is not good'
  }
  const backwards = [];
  const totalItems = str.length -1;
  for (let i = totalItems; i >= 0; i--) {
    backwards.push(str[i]);
  }

  return backwards.join(' ')
}
console.log(reverse("Hi i am emir"))


~~~

