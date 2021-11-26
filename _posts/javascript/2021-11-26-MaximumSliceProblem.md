---
layout post
title "Maximum Slice Problem"
comments true
share true
modified
categories javascript
excerpt
tags []
image
  feature
date 2021-11-26T153955-0400
modified 2021-11-26T153955-0400
---

##Maximum Slice Problem

The problem is to find the maximum sum of a sub-array of a given integer array. The strategy is to keep track of the sum of current element + previous element and compare it to the current element to find the local max.


Examplebr
console.log(solution([4,8,2,6,7],[0,1,1,0,0])); = 2 br
console.log(solution([4,3,2,1,5],[0,1,0,0,0])); = 2 br




~~~
function solution(A, B) {
  let stack = [];
  let survivors = 0;

  for(let i = 0; i  A.length;i++){
    let weight = A[i];
    if (B[i]=== 1) {
      stack.push(weight)
    } else {
      let weightDown = stack.length === 0  -1  stack.pop();
      while(weightDown !== -1 && weightDown  weight)
          weightDown= stack.length === 0  -1  stack.pop();
      if (weightDown === -1) 
        survivors +=1;
       else 
        stack.push(weightDown);      
    }
  }

  return survivors + stack.length;
}

console.log(solution([4,8,2,6,7],[0,1,1,0,0])); 2
console.log(solution([4,3,2,1,5],[0,1,0,0,0])); 2
~~~
___
We create a function called Solution with parameters called A and B we create an array called stack and counter called survivors = 0 to hold all of the numbers;
<br>
We loop with for of loop to loop from 0 untill i is less than A.lenght, then we increment
<br>
We create a variable named weight to hold A[i] variables. Then we do If statement to check if 
B[i]=== 1; And if it is we use the temporary variable array variable stack to push the new item weight.
<br>
Else we create another temporary variable weightDown that is equal to if  stack.length === 0 or () -1 Else () stack.pop(); we remove item from the end. 
<br>
I want to mention I have used turnery operators so you probably need to check them to.
<br>
Then we do another loop while loop to check these conditions weightDown = stack.length === 0  
(true) return -1  (or) stack.pop()
<br>
The we use weightDown = to check stack.length === 0  -1  stack.pop()
<br>
We do another if conditional to check if weightDown === -1 we increment survivors by 1
Else stack.pop(weightDown)
<br>
In the end we return survivors + stack.length;


