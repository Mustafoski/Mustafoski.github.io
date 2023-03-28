---
layout: post
title: "Sorting with Comparator function"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2023-03-28T15:39:55-04:00
modified: 2023-03-28T15:39:55-04:00
---

Sorting with Comparator Function
<br><br>

Sorting with a comparator function means that a function is passed as an argument to the sort() method of an array to define the order in which the elements of the array should be sorted based on the comparison of two elements at a time, and the return value of the function determines their position in the sorted array.

**Example**<br>
let numbers = [57, 34, 10, 23, 7, 100]; and let strings = ['Banana', 'Orange', 'Apple', 'Blueberry'];
<br><br>
All possible sums of 2 consecutive elements are <br>
[7,10,23,34,57,100]<br>
['Apple', 'Banana', 'Blueberry', 'Orange']<br>




~~~
let numbers = [57, 34, 10, 23, 7, 100];
let strings = ['Banana', 'Orange', 'Apple', 'Blueberry'];

numbers.sort(function(a,b) {
  return a - b
  });
  strings.sort();

  console.log(numbers)
  console.log(strings)
~~~



This code sorts two arrays, numbers and strings, using the sort() method. The sort() method is used to sort the elements of an array in ascending order by default.<br><br>

To sort the numbers array in ascending order, a compare function is passed as an argument to the sort() method. The compare function takes two parameters a and b, representing two elements of the array to be compared. The function subtracts b from a and returns the result. If the result is negative, a comes before b, if it is positive, b comes before a, and if it is zero, no changes are made. This way, the sort() method can compare and sort the numbers in the array in ascending order.
<br><br>
To sort the strings array in alphabetical order, no compare function is passed to the sort() method since strings are already comparable. The sort() method sorts the strings array in alphabetical order.<br><br>

Finally, the console.log() method is used to display the sorted numbers and strings arrays in the console.