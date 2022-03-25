---
layout: post
title: "Alphabetic SubSequence"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-03-11T15:39:55-04:00
modified: 2022-03-11T15:39:55-04:00
---

Alphabetic SubSequence
<br>
Check whether the given string is a subsequence of the plaintext alphabet.


**Example**<br>

- For s = "effg" or s = "cdce", the output should be<br>
alphabetSubsequence(s) = false<br>

- For s = "ace" or s = "bxz", the output should be<br>
alphabetSubsequence(s) = true.<br>




~~~
function alphabetSubsequence(s) {
  const chars = s.split('');
  const charValues = []

  chars.forEach(char => {
    charValues.push(char.charCodeAt(0))
  });
  if (new Set(charValues).size !== charValues.length) {
    return false
  }
  for (let i = 0; i < charValues.length - 1; i++) {
    if (charValues[i] >= charValues[i + 1]) {
      return false
    }
    }
  return true

}

console.log(alphabetSubsequence('zab')) false 
console.log(alphabetSubsequence('effg')) false 
console.log(alphabetSubsequence('cdce')) false
console.log(alphabetSubsequence('ace')) true
console.log(alphabetSubsequence('bxz')) true

~~~



We create function called alphabetSubsequence with parameter **s** and local variable **chars = s.split('')**  and **charValues = []**<br><br>
The split() method divides a String into an ordered list of substrings, puts these substrings into an array, and returns the array. The division is done by searching for a pattern; where the pattern is provided as the first parameter in the method's call. - **MDN**
<br><br>
We do a forEach loop on **chars** array  and with callback function and parameter *char* we push **charValues.push(char.charCodeAt(0)**
<br><br>
The charCodeAt() method returns an integer between 0 and 65535 representing the UTF-16 code unit at the given index. - **MDN**
<br><br>
If we use Set function to delete any duplicates **new Set(charValues).size !== charValues.length** if true we return false
<br><br>
We loop again with for loop this time to see the starting value (0) and until the last remainding value **charValues.lenght - 1** and we increment by 1
<br><br>
Inside the for loop we check if **charValues[i] >= charValues[i + 1]** and if it is we return false again. 
<br><br>
So if all the cases above are false we **return true**