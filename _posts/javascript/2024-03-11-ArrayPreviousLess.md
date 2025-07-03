---
layout: post
title: "Array Previous Less"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2023-02-15T15:39:55-04:00
modified: 2023-02-15T15:39:55-04:00
---

Array Previous Less
<br><br>

Given array of integers, for each position i, search among the previous positions for the last (from the left) position that contains a smaller value.Store this value at position i in the answer.If no such value can be found store -1 instead.
**Example**<br>
For Input: inputArray = [3,5,2,4,5] the output should be bubbleSort will be [-1,3,-1,2,4]

<br>
Solution: [-1,3,-1,2,4]

<br>


```
function arrayPreviousLess(items) {
  const lessThanList = [];
  for (let i = items.length - 1; i >= 0; i--) {
    for (let j = i; j >= 0; j--) { 
      if (items[i] > items[j]) {
        lessThanList.unshift(items[j]);
        break;
      } else if (j === 0) {
        lessThanList.unshift(-1);
      }
    }
  }

  return lessThanList;
}

console.log(arrayPreviousLess([3, 5, 2, 4, 5]));

```
Initialize an empty array lessThanList to store the result.
Iterate over the input array items in reverse order, starting from the last element.
For each element at index i in the input array:
Start an inner loop from i down to 0.
If the element at index i is greater than the element at index j, add the element at index j to the beginning of lessThanList using unshift method.
If the inner loop reaches the first element (index 0) and no element is found to be less than the element at index i, add -1 to the beginning of lessThanList.
Return the lessThanList array containing the first elements less than the corresponding elements in the input array.


