---
layout: post
title: "BinarySearch"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-04-18T15:39:55-04:00
modified: 2021-04-18T15:39:55-04:00
---

## BinarySearch
<br>
In computer science, binary search, also known as half-interval search, logarithmic search, or binary chop, is a search algorithm that finds the position of a target value within a sorted array. Binary search compares the target value to the middle element of the array.
___

> ##For Example
[5, 7, 12, 16, 36, 39, 42, 56, 71], 56
Should return true<br>
##
<br>

___


~~~
function binarySearch(numArray, key) {
    var middleIdx = Math.floor(numArray.length / 2);
    var middleElem = numArray[middleIdx];
    
    if (middleElem === key) return true;
    else if (middleElem < key && numArray.length > 1) {
        return binarySearch(numArray.splice(middleIdx, numArray.length), key);
    }
    else if (middleElem > key && numArray.length > 1) {
        return binarySearch(numArray.splice(0, middleIdx), key);
    }
    else return false;
}

binarySearch([5, 7, 12, 16, 36, 39, 42, 56, 71], 56);

~~~

___

