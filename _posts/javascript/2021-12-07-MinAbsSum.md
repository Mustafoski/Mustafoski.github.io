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
console.log(solution([-7,3,-1,5,-11,-9,14,17,-2])) =>1 <br> 
console.log(solution([8,3,5,16,11]))   =>6            <br>  
console.log(solution([-7,-5,-6,-2,-9]))   =>4     <br> 
console.log(solution([-7,3,-6,1,0,-9])) => 0 <br> 
console.log(solution([-22,3,4,5])) => 6 <br> 
<br> 




~~~
function solution(input) {
  let minAbsSumOfTwo = Number.MAX_VALUE;
  input.sort((a,b) => a - b);
  let head = 0
  let tail = input.length -1;
  while(head <= tail) {
    minAbsSumOfTwo = Math.min(minAbsSumOfTwo,Math.abs(input[head]+ input[tail]));
    if(input[head] + input[tail] < 0) head ++; 
    else tail --;
  }
  return minAbsSumOfTwo;
}

console.log(solution([-7,3,-1,5,-11,-9,14,17,-2]))
console.log(solution([8,3,5,16,11]))
console.log(solution([-7,-5,-6,-2,-9]))
console.log(solution([-7,3,-6,1,0,-9]))
console.log(solution([-22,3,4,5]))

~~~
___
We create a function called solution with parameter called *input*.
<br><br>
First in this function we create a variable that will hold our solution and we called *minAbsSumOfTwo* = Number.MAX_VALUE; Number.MAX_VALUE is the number largest max integer
 <br>
Then we need to sort the *input* like this input.sort((a, b) => )
<br><br>
Next we need to initialize our two pointers, the red and blue arrows and we shall call them the first one had to give its a value of 0 and the next one to be tail
<br><br>
First one we shall call *head* = 0; second tail = input.length - 1;
<br><br>
Next we need while loop to check while(head <= tail) {
  minAbsSumOfTwo = Math.min(minAbsSumOfTwo, Math.abs(input[head]+ input[tail]));
  if (input[head]) + input[tail] < 0) head ++;
  else tail--;
}
<br><br>
While *head* was smaller or equal to tail we loop with while loop and inside we calculate <br>
minAbsSumOfTwo = Math.min(minAbsSumOfTwo), Math.abs(input[head] + input[tail]);
<br>
Math.min and Math.abs are JavaScript build in methods
Math.min = > The static function Math.min() returns the lowest-valued number passed into it, or NaN if any parameter isn't a number and can't be converted into one. [MDN]<br>
Math.abs = > The Math.abs() function returns the absolute value of a number. That is, it returns x if x is positive or zero, and the negation of x if x is negative.[MDN]<br>
<br><br>
We check if input[head] + input[tail] < 0 and if it is head ++ else tail ++
<br>
In the end we return *minAbsSumOfTwo*;


