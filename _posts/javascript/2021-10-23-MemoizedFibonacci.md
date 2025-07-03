---
layout: post
title: "Memoized Fibonacci"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-10-23T15:39:55-04:00
modified: 2021-10-23T15:39:55-04:00
---

## Memoized Fibonacci

Memoized Fibonacci

Example:<br>
MemoizedFibonacci(12); 144  <br>
MemoizedFibonacci(8); 21 <br>
MemoizedFibonacci(15); 610  <br>




~~~
function MemoizedFibonacci(index, cache) {
  cache = cache || [];

  if (cache[index]) return cache[index];
  else {
    if (index < 3) return 1;
    else {
      cache[index] = MemoizedFibonacci(index-1,cache)+ MemoizedFibonacci(index-2,cache);
    }
  }
  return cache[index]
}

MemoizedFibonacci(12); 144
MemoizedFibonacci(8); 21
MemoizedFibonacci(15); 610

~~~
___

We create a function MemoizedFibonacci with parameters of index and cache we use cache = cache || [] which is essentialy as the second parameter when invoking is empty array <br>

The base is when we check if cache has the index and if it does it returns the cache of index<br>

In the else clause we check recursively and used cache[index] = MemoizedFibonacci(index-1,cache)+ MemoizedFibonacci(index-2,cache); This is familiar from basic recursively Fibonacci   <br>

In the end we return cache[index] since we store the recursively function in cache[index];

