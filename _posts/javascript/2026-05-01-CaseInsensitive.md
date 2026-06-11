---
layout: post
title: "IsCaseSensitivePalindrome"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2026-04-11T15:39:55-04:00
modified: 2026-04-11T15:39:55-04:00
---




# IsCaseSensitivePalindrome



 ###Given a string check if it can becomee palindrome through a case change or some letterst
 ---
 ```
function isCaseInsensitivePalindrome (inputString ) {
  const originalLowerCase = inputString.toLowerCase();
  const reversedWord = originalLowerCase.split("''").reverse().join()

  return originalLowerCase === reversedWord
}

console.log(isCaseInsensitivePalindrome('AaBaaa')) true

console.log(isCaseInsensitivePalindrome('aabaaa')) false
```


---

## Implementation Details

* **Parameter:**
  * `inputString`: The string to be checked.

* **Logic:**
  * Convert the string to lowercase using `toLowerCase()` to ensure case-insensitive comparison.
  * Split the string into individual characters using `split("")`.
  * Reverse the array using `reverse()`.
  * Join it back into a string using `join("")`.
  * Compare the original normalized string with the reversed string.
  * If both are equal → return `true`, otherwise return `false`.

---


