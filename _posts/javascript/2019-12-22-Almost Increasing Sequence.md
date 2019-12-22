---
layout: post
title: "Almost Increasing Sequence"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2019-12-22T15:39:55-04:00
modified: 2019-12-22T15:39:55-04:00
---

## Almost Increasing Sequence


An almost increasing sequence can only have one number that is smaller than its previous number, and it must not equal than the number before its previous number. Also, the previous number must not equal to the number after the current number.

 
___

> ##For Example
For  sequence = [1,3,2,1] the return false<br>
For  sequence = [1,3,2] the return true <br>

Should return true<br>
##
<br>

___


~~~

let sequence = [1,3,2]
let sequence1 = [1,3,2,1]



function almostIncreasingSequence(sequence) {
  let count = 0;
  
  for(let i = 0; i<sequence.length; i++) {
    if(sequence[i] <= sequence[i - 1]){
      count ++;
      
      if(sequence[i] <= sequence[i - 2] && sequence[i+1] <= sequence[i-1]){
        return false;
      }
    }
  }
  
  
  
  return count <= 1;
}

console.log(almostIncreasingSequence(sequence))
console.log(almostIncreasingSequence(sequence1))

~~~

___

1. After creating function we create counter variable as count = 0;
2. We loop the array and check if current number is less or equal than previous number if yes then we increase hence we increase count ++ by 1.
3. Then we use one more if statement to check if two times increases Also, the previous number must not equal to the number after the current number.
