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




⚙️ Implementation Details
Parameters
year (Number): The year for which the century needs to be determined (e.g., 1905, 1700).

Step-by-Step Logic
Divide the year by 100 to calculate its base century value.

Evaluate whether the year is evenly divisible by 100 using the modulo operator (year % 100 === 0).

Exact Centuries: If the remainder is 0, the year falls exactly at the end of a century (like 1700 or 2000). In this case, simply return the calculated century value.

Partial Centuries: If there is a remainder, it means the year is partway through the next century. Round the base calculation down using Math.floor() and add 1 to get the correct, current century.

Return the final calculated century number.

---