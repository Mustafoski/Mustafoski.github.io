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

In computer science, the maximum sum subarray problem is the task of finding a contiguous subarray with the largest sum, within a given one-dimensional array A[1...n] of numbers.

Example:<br>
console.log(Brackets("()[]()[]{}")) 1 <br>
console.log(Brackets("([{}])")) 1 <br>
console.log(Brackets("()]]"))  0 <br>




~~~
function Brackets(input) {
  let stack = [];
  for(const c of input) {
    if (c === '{' || c === '[' || c === '(' ){
      stack.push(c);
    } else if (c ===  '}') {
      if(stack.length === 0 || stack.pop() !== '{') return 0;
    }else if (c ===  ']') {
      if(stack.length === 0 || stack.pop() !== '[') return 0;
    }else if (c ===  ')') {
      if(stack.length === 0 || stack.pop() !== '(') return 0;
}
    }
    return stack.length ? 0 : 1
  }

console.log(Brackets("()[]()[]{}"))
console.log(Brackets("([{}])"))
console.log(Brackets("()]]"))

~~~
___
We create a function called Brackets with parameter called *input* and we create an array called    *stack* to hold all of the brackets;
<br>
We loop with for of loop where we create variable c of input and we check if c is '(' or c is '{' or c is '[' opening parenthesis. And if we find we push into the array variable stack with JavaScript push method.
<br>
Then we create 3 if else statements for each of the individual parenthesis so we have else if we have closed parenthesis 
<br>
1st else if (c ===  '}')
We check if the stack.length === 0 or stack.pop() pop() is another JavaScript method that take the last added in this case stack.pop() is not equal to the '{' we return 0 which means it faild
<br> 
2nd else if (c ===  ']')
We check if the stack.length === 0 or stack.pop() pop() is another JavaScript method that take the last added in this case stack.pop() is not equal to the '[' we return 0 which means it faild
<br>
3rd else if (c ===  ')')
We check if the stack.length === 0 or stack.pop() pop() is another JavaScript method that take the last added in this case stack.pop() is not equal to the '(' we return 0 which means it faild
 <br>
At the end we return stack.length ? (true => there is something left) 0 : 1
<br>


