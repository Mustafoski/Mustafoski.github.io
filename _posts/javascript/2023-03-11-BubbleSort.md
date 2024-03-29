---
layout: post
title: "Buble Sort"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2023-02-14T15:39:55-04:00
modified: 2023-02-14T15:39:55-04:00
---

Bubble Sort 
<br><br>

Given an array, find the maximal sum difference between any two of its adjacent elements.
**Example**<br>
For Input: inputArray = [5, 3, 8, 2, 1, 4] the output should be bubbleSort will be [ 1, 2, 3, 4, 5, 8 ]

<br>
Solution: [ 1, 2, 3, 4, 5, 8 ]

<br>


```
function bubbleSort(array) {
  for (let i = array.length; i > 0; i--) {
    for (let j = 0; j < i; j++) {
      if (array[j] > array[j + 1]) {
        let temp = array[j];
        array[j] = array[j + 1];
        array[j + 1] = temp;
      }
    }
  }
  return array;
}

console.log(bubbleSort([5, 3, 8, 2, 1, 4]));
[ 1, 2, 3, 4, 5, 8 ]
```
Outer Loop: The outer loop iterates over the array in reverse order, starting from the last element (array.length) and decrementing i until it reaches 0. This loop controls the number of passes through the array.

Inner Loop: Within the outer loop, there's an inner loop that iterates over the array from index 0 to i - 1. This loop compares adjacent elements and swaps them if they are in the wrong order (i.e., if array[j] is greater than array[j + 1]).

Swapping: The swapping is done using a temporary variable temp to hold the value of array[j] before it's overwritten by array[j + 1]. This ensures that the original value of array[j] is preserved during the swap.

Bubble Up: After completing each pass through the array, the largest unsorted element "bubbles up" to its correct position at the end of the array.

Return: The function returns the sorted array after completing all passes.


