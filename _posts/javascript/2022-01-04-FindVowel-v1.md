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
date: 2022-01-07T15:39:55-04:00
modified: 2022-01-07T15:39:55-04:00
---

## Find Vowel-v1
We write a function that returns the number of vowels used in a string. Vowels are characters 'a' ,'e', 'i', 'o' and 'u'


Example:<br>
vowels('Hi There!') --> 3<br>
vowels('Why do you ask?') --> 4<br>
vowels('Why?') --> 0<br>
<br>





~~~
function extractValue(arr, key){
    return arr.reduce(function(acc,next){
        acc.push(next[key]);
        return acc;
    },[]);
}

let arr = [[1,2,3],[2,3,4],[3,4,5],[4,5,6],[5,6,7]];
let key = 2;

console.log(extractValue(arr,key)) [3, 4, 5, 6, 7]

let arr = [[1,2,3],[2,3,4],[3,4,5],[4,5,6],[5,6,7]];
let key = 1;
console.log(extractValue(arr,key)) [2, 3, 4, 5, 6]
~~~
___
We create a function called vowelCount with parameter called *str* and variable calledd *vowels* that is equal to every vowel "aeiou"
<br><br>
We return *str*.toLowerCase().split('').reduce(function(acc,next) {})<br>
We turn *str* to lowercase with toLowerCase JavaScript Method nad than we use split('') like this to turn that string into an array. then we chain reduce wich returns callback function with parameters *acc* and *next*
<br><br>
 if(vowels.indexOf(next) !== -1){ we check if vowels with .indexOf another JavaScript Method
<br>
The indexOf() method returns the first index at which a given element can be found in the array, or -1 if it is not present. -MDN 
<br><br>
Then we check <br>
if(acc[next]){<br>
  acc[next]++;<br>
} else {<br>
  acc[next] = 1;<br>
  }<br>
  return acc;<br>
<br><br>
If *acc*[*next*] is vowel and if it is we increase with acc[next]++<br>
else  if it only found vowel once acc[next] = 1;<br>
In the end we return the *acc*