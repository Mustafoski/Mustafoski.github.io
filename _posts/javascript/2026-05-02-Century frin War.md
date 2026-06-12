---
layout: post
title: "Century from war"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2026-04-12T15:39:55-04:00
modified: 2026-04-12T15:39:55-04:00
---




# Century from war



 ### Given a year, return the century it is in. The first century spans from year 1 up to and including the year 100, the second - from year 101 up to and including the year 200 , etc.
 ---
 ```
function centuryFromYear(year) {
  const century = year / 100;

  if (year % 100 === 0) {
    return century;
  }


  return Math.floor(century) + 1
}

console.log(centuryFromYear(1905)) 20 
console.log(centuryFromYear(1700)) 17

```



---
# Implementation Details

## Parameter
year: The year for which the century needs to be determined.

## Logic
       Divide the year by 100 to calculate its century value.
       Check whether the year is evenly divisible by 100.
       If the remainder is 0, the year falls at the end of a century, so return the calculated century.
       Otherwise, round the result down using Math.floor() and add 1 to get the correct century.
       Return the resulting century number.

---