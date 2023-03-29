---
layout: post
title: "Sorting with Comparator function v2"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2023-02-10T15:39:55-04:00
modified: 2023-02-10T15:39:55-04:00
---

Sorting with Comparator Function v2
<br><br>

Sorting with a comparator function means that a function is passed as an argument to the sort() method of an array to define the order in which the elements of the array should be sorted based on the comparison of two elements at a time, and the return value of the function determines their position in the sorted array.

**Example**<br>
let numbers = [57, 34, 10, 23, 7, 100]; and let strings = ['Banana', 'Orange', 'Apple', 'Blueberry'];
<br><br>
All possible sums of 2 consecutive elements are <br>
[7,10,23,34,57,100]<br>
['Apple', 'Banana', 'Blueberry', 'Orange']<br>




~~~
let numbers = [57,34,10,23,7,100];
let strings = ['Banana', 'Orange', 'Apple','Blueberry']

numbers.sort(function(a,b) {
    if (a > b) {
        return 1;
    }
    if (a < b) {
        return -1;
    }
    return 0;
});
strings.sort();
console.log(numbers)
console.log(strings)
~~~


This code demonstrates the use of the sort() method in JavaScript. The code creates two arrays: numbers and strings. The numbers array contains a list of integers, and the strings array contains a list of strings.<br><br>

The first part of the code sorts the numbers array using a function passed as an argument to the sort() method. The function compares two elements of the array, a and b, and returns -1, 0, or 1 depending on whether a is less than, equal to, or greater than b. This sorting function sorts the numbers in ascending order.<br><br>

The second part of the code sorts the strings array using the default sorting algorithm, which sorts strings in lexicographic order (i.e., alphabetical order).<br><br>

Finally, the code prints the sorted numbers and strings arrays to the console using console.log().
<br><br>
In summary, this code demonstrates the use of the sort() method to sort arrays in JavaScript, and also demonstrates how to use a custom sorting function for more complex sorting requirements.
<br><br>