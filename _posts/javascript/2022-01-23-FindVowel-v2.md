---
layout: post
title: "Find Vowel-v2"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-01-23T15:39:55-04:00
modified: 2022-01-23T15:39:55-04:00
---

## Find Vowel-v2
We write a function that returns the number of vowels used in a string. Vowels are characters 'a' ,'e', 'i', 'o' and 'u'


Example:<br>
vowels('Hi There!') --> 3<br>
vowels('Why do you ask?') --> 4<br>
vowels('Why?') --> 0<br>
<br>





~~~
function vowels(str) {
const matches = str.match(/[aeiou]/gi);
  return matches ? matches.length : 0;
}
~~~
___
We create a function called vowels with parameter called *str* and variable called *matches* 
<br><br>
***const matches = str.match(/[aeiou]/gi);***
<br><br>
So we are going to look at the *str* parameter and call match method on the *str*. Match is used to see if some possible thing is included inside of this string.
<br>
So we can pass regular expression and this regular expression is going to check to see if we have we have any vowels inside.
<br><br>
Regular expression is going to have a pair of square braces when put in square pair of square. And inside the braces we put the vowels to check if this string contains any character that is inside of the square brackets right here then let us know. So we are going to put all the characters that we care about [aeiou]
<br><br>
The other thing we are going to do is add to options to regex itself /gi<br>
The g in regular expression represent global and i represent case insensitive 
<br><br>
So we store that in the *matches* variable and if there is vowel it will return an array otherwise it will return <b>null<b>
  <br><br>
Null is considered falsy value and an array is considered truthy value. So we do<br>
***return matches ? matches.length : 0;***