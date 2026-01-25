---
layout: post
title: "Find Vowel-v1"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-01-04T15:39:55-04:00
modified: 2022-01-04T15:39:55-04:00
---

## Find Vowel-v1
We write a function that returns the number of vowels used in a string. Vowels are characters 'a' ,'e', 'i', 'o' and 'u'


Example:<br>
vowels('Hi There!') --> 3<br>
vowels('Why do you ask?') --> 4<br>
vowels('Why?') --> 0<br>
<br>





~~~
function vowels(str) {
  let count = 0;
  const vowelCheker = "aeiou";
  for (let char of str.toLowerCase()) {
    if (vowelCheker.includes(char)) {
      count++;
    }
  }
  return count;
}
~~~
___
We create a function called vowels with parameter called *str* and variable called *count* that is equal to 0 and *vowelChecker* equal to "aeiou"
<br><br>
We loop with for of loop but we make the *str* parameter toLowerCase() to check even if vowel is uppercased.
<br><br>
 Inside the loop we check if *vowelChecker*.includes(char)
<br>
The includes() method determines whether an array includes a certain value among its entries, returning true or false as appropriate. -MDN 
<br><br>
If includes returns true we increment count by 1 with count++
<br><br>
In the end we return the *count*