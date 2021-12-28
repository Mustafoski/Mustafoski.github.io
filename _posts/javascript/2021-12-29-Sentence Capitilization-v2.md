---
layout: post
title: "Sentence Capitalization-v2"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-12-28T15:39:55-04:00
modified: 2021-12-28T15:39:55-04:00
---

## Sentence Capitalization v2

<br>

Write a function that accepts a string. The function should capitalize the first letter of each word in the string then return the capitalized string.

<br>
Examples <br>
capitalize('a short sentence') => return 'A Short Sentence<br>
capitalize('a lazy fox') => return 'A Lazy Fox'<br>
capitalize('look, it is working!') => return 'Look, It Is Working'
<br>

~~~
function capitalize(str) {
  let result = str[0].toUpperCase();
  for (let i = 1; i < str.length; i++) {
    if (str[i - 1] === ' ') {
      result += str[i].toUpperCase();
    } else {
      result += str[i];
    }
  }
  return result;
}
}
~~~
___

<br><br>
First we create function capitalize with parameter *str* and create variable *result* equal to str[0].toUpperCase(). So we take the first letter and Capitilize.
<br><br>
Then we do for loop starting with 1 looping untill length of the *str* and for each iteration we add 1;
<br><br>
Inside the loop we check if *str*[i-1] === ' ' and if they do we take that letter ***i*** and use it like str[*i*].toUpperCase()
<br><br>
All of these is added into *result* variable with concatination += str[i].toUpperCase()
<br><br>
Else *result* is equal to result + str[i] which means there is no empty space so the letters are downcase except the first one.
<br><br>
In the end we return *result*