---
layout: post
title: "Max Non Overlapping Segments"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-12-08T15:39:55-04:00
modified: 2021-12-08T15:39:55-04:00
---

## From *Codility*  Max Non Overlapping Segments"

We are given number of segments and we need to find the maximum number of this segments of those segments that do no overlap another one.<br>
These segments that we are given in the input of our function are ordered by the ending position of each segment.


Example:<br>
console.log(solution([1,3,7,9,9],[5,6,8,9,10]))  => 3
<br> 




~~~
function solution (start, end) {
  let lastEndSegment = -1;
  let choosenCount = 0;

for(let i = 0; i < start.length;i++) {
  if (start[i] > lastEndSegment){
    choosenCount++;
    lastEndSegment = end[i]
  }
}
  return choosenCount;
}

console.log(solution([1,3,7,9,9],[5,6,8,9,10]))  => 3
~~~
___
We create a function called solution with parameters called *start* and *end*. Each of this parameter is a list and each element in the list represents the start and the end of each segment.
<br><br>
We need couple variables *lastEndSegment* = - 1; and *choosenCount* = 0 and *choosenCount* will return the solution.
<br>
Then we create for loop where i = 0; i < start.length; i++
Inside the loop we check if(*start*[i] > lastEndSegment) 
<br><br>
If the check is true we increment by one *choosenCount* and we reset the last and segment variable to be the end position of this particular segment which is *end*[i]
<br><br>
In the end we return *countChoosen*


