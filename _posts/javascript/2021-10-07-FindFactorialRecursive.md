---
layout: post
title: "FindFactorialRecursive"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-07-18T15:39:55-04:00
modified: 2021-07-18T15:39:55-04:00
---

## FindFactorialRecursive

Finding wether if algorithm can works recorsevily

Example:<br>
console.log(ArrayConvertion([1,2,3,4,5,6,7,8])) 186 <br>




~~~
function findFactorialRecurative(number) {
  let answer = 1;
  if (number === 2) {
    answer = 2;
  }
  for (let i = 2; i < number; i++ ){
    answer = answer*i;
  }
  return answer
}

findFactorialRecurative(5)} 24

}

~~~
___

We create a function findFactorialRecurative with parameter of number and we create a variable answer to be equal to 1 so we can keep track if the elements <br>

We check wheter number is equal to 2 and if it is we assing answer to 2.<br>

We loop the remaining by starting with i to be equal to 2 then i is less than number and we increment by 1. Inside the loop we take answer variable and with If statement check if number is equal to 2. If it is we assing asnwer to2 <br>

In the end we return answer

