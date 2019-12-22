---
layout: post
title: "Add Border"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2019-09-29T15:39:55-04:00
modified: 2019-09-29T15:39:55-04:00
---

## Add Border

Outside of the values we give border with the style of *

___

> ##For Example
For picture = ["abc","ded"] the output should be ["*****", "*abc*", "*ded*", "*****"]<br>

Should return true<br>
##
<br>

___


~~~
let picture = ["abc","ded"];

function addBorder(picture) {
  const wall = '*'.repeat(picture[0].length + 2);
  
  picture.unshift(wall);
  picture.push(wall);
  
  for(let i = 1; i< picture.length - 1;i++) {
    picture[i] = '*'.concat(picture[i],'*');
  }
  
  return picture;
}

console.log(addBorder())

~~~

___

1. First we create const wall where we use String method repeat of * where inside picture start at 0 index to 2 index;
2. Then we use another String Method unshift the picture (before the values) and we put it wall;
3. Again we use String Method push where instead (before the values ) we push it after the values the wall;
4. Lastly we use for loop to loop through the values But remember we start with * and end with * so that is why i = 1 and i< picture.lenght -1;
5. Then we plug the * with another String method concat we use one before the values and one after
6. Last we return the full picture