---
layout: post
title: "FibonacciIterative"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-10-09T15:39:55-04:00
modified: 2021-10-09T15:39:55-04:00
---

## FibonacciIterative

Finding wether if algorithm can works recorsevily

Example:<br>
fibonacciIterative(8) 21  <br>




~~~

function fibonacciIterative(n) {
  let arr = [0,1]
  for(let i = 2; i < n + 1; i++) {
    arr.push(arr[i-2]+ arr[i-1])
  }

  return arr[n]
}
fibonacciIterative(8) 21
~~~
___

We create a function fibonacciIterative with parameter of number <br>
We create an array called *arr* that holds 0 and 1.<br>
We create a for loop where we start from 2 where i is less than n + 1 and we increment by 1 <br>
We use JavaScript build in method push to push to the *arr* (arr[i-2] + arr[i-1])


We return arr[n] <br>

In the end we return answer

