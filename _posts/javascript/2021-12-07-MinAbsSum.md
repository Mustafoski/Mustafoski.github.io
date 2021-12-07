---
layout: post
title: "Min ABS SUM"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-12-07T15:39:55-04:00
modified: 2021-12-07T15:39:55-04:00
---

## From *Codility* 

In this puzzle, we are given an input list of numbers and these numbers can be negative or positive
and we need to find two of these numbers represented over a year by the Pointer P and Q such that when you sum the value at P and the value of Q you get a result.<br>
And if you put that result into an absolute function, the result will be a minimum.

Example:<br>

<br> 




~~~


~~~
___
We create a function called Solution with parameters called *a*, *b*.
<br><br>
We us the if statement to check if ( *b* === 0) if it is we return *a*
 <br>
Else we return findGcd function and inside parameters return findGcd(*b*, *a* % *b*);
<br><br>
We create the main function called solution with parameters *N* and *M* and simply we return *N* / findGcd(N, M);
<br><br>
So to print the values we use console.log build in function console.log(solution(10,4)); and it returns 5


