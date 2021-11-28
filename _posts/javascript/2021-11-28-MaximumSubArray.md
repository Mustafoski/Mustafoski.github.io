---
layout: post
title: "Maximum Sub Array"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-11-28T15:39:55-04:00
modified: 2021-11-28T15:39:55-04:00
---

## Maximum Sub Array

The problem is to find the maximum sum of a sub-array of a given integer array. The strategy is to keep track of the sum of current element + previous element and compare it to the current element to find the local max.

Example:<br>
console.log(solution([4,8,2,6,7],[0,1,1,0,0])); = 2 <br>
console.log(solution([4,3,2,1,5],[0,1,0,0,0])); = 2 <br>




~~~
function solution(A, B) {
  let stack = [];
  let survivors = 0;

  for(let i = 0; i < A.length;i++){
    let weight = A[i];
    if (B[i]=== 1) {
      stack.push(weight)
    } else {
      let weightDown = stack.length === 0 ? -1 : stack.pop();
      while(weightDown !== -1 && weightDown < weight)
          weightDown= stack.length === 0  ? -1 : stack.pop();
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
We create a function called solution with parameter called *A* and *B* we create an array called    *stack* and variable *survivors* that we initialize to 0;
<br><br>
We loop with for of loop for(let i = 0; i < A.length;i++) then we create variable weight equals to A[i]
<br><br>
Inside the for loop we check with if condidition if (B[i]=== 1) and if true we use build in JavaScript method push() to push *weight* to array *stack*
<br><br>
Else we create variable weightDown if weightDown is stack.length === 0 we return -1 else we use another build in JavaScript method pop() which removes the last element from an array and we use stack array to pop with stack.pop(). 
<br> <br> 
Then we use another loop called while loop that checks weightDown !== -1 && weightDown < weight then again we check if weightDown is stack.length === 0 we return -1 else we pop() from stack array with stack.pop() 
<br><br>
Inside the while loop we check if (weightDown === -1) if true we increment *survivors* by 1
 <br>
Else we push into stack array with stack.push(weightDown)
<br><br>
In the end we return *survivors* + stack.length


