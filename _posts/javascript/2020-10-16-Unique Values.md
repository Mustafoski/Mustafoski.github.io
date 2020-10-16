---
layout: post
title: "Unique Values-v2"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2020-10-16T15:39:55-04:00
modified: 2020-16
-15T15:39:55-04:00
---

## Unique Values-v2

Unique Values is when in a string every letter is unique if they are all different unique then it is true of not like the second example if there are duplicates than it is false
___

> ##For Example<br>
  abcde => true<br>
 abcda => false<br>
>
##
<br>

___

~~~

function unique(str){

  let tempStr = new Set();

  for(let letter of str){
    if(tempStr.has(letter)){
      return false;
    }
    tempStr.add(letter)
  }

  return true;
}

console.log(unique('abcd')) => true
console.log(unique('abcdade')) => false
~~~

function unique(str){ <br><br>

First we create a function called unique and pass an argument string called str.

<br><br>

let tempStr = new Set();
<br><br>

First we know that we will work with Set data structure so we start very simply and create that new data structure called let tempStr = new Set(). And what is unique about the Set data structure it only accepts unique values. Meaning if you trying to pass something that is already in there it will not be accepted.

<br><br>
for(let letter of str){ <br>
    if(tempStr.has(letter)){ <br>
    return false; <br>
    } <br>
  tempStr.add(letter)<br>

<br><br> 

The way we can do that is to create for of loop where we will loop through the string, and check if it is already in the Set if it is we return false of not otherwise we will add that letter to the tempStr. We say let letter of string that is passed on. We check if the tempStr and Set method has and it will look like if (tempStr.has(letter)) so if the tempStr has the letter we return to false.

Other than that we use another Set method like push method called add method and we say. tempStr.add(letter). This is how we add or push with Set data structure.


<br><br>

return true;

 
<br><br>

Now if everything works smoothly and we don't have repeating letter we return true.


<br><br>

