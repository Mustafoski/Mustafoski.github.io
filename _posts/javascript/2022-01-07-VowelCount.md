---
layout: post
title: "Vowel Count"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-01-06T15:39:55-04:00
modified: 2022-01-06T15:39:55-04:00
---

## Vowel Count
Vowel Count is counting the vowels (a,e,i,o,u) from string.


Example:<br>
console.log(vowelCount('Emir Mustafoski'))<br>
[object Object] {
  a: 1,
  e: 1,
  i: 2,
  o: 1,
  u: 1
}<br>
console.log(vowelCount("Natalie Portman"))<br>
[object Object] {
  a: 3,
  e: 1,
  i: 1,
  o: 1
}<br>





~~~
function vowelCount(str){
    var vowels = "aeiou";
    return str.toLowerCase().split('').reduce(function(acc,next){
        if(vowels.indexOf(next) !== -1){
            if(acc[next]){
                acc[next]++;
            } else {
                acc[next] = 1;
            }
        }
        return acc;
    }, {});
}

console.log(vowelCount('Emir Mustafoski'))
console.log(vowelCount("Natalie Portman"))
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