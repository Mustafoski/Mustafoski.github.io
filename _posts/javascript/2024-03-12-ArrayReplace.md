---
layout: post
title: "Array Replace"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2024-03-12T15:39:55-04:00
modified: 2024-03-12T15:39:55-04:00
---

Alphabetic Shift
<br>
Given an array of integers, replace all the occurence of elemToReplace with subtitutionElem.




**Example**<br>
- For inputArray = [1,2,1], the output should be
<br>
elemToReplace = 1 and substitutionElem = 3 , the output should be arrayReplace(inputArray,elemToReplace,substitutionElem) = [3,2,1]




~~~
function arrayReplace(inputArray, elemToReplace, substitutionElem) {
  inputArray.forEach((element, index) => {
    if (element === elemToReplace) {
      inputArray[index] = substitutionElem;
    }
  });
  return inputArray;
}

console.log(arrayReplace([1, 2, 1], 1, 3)); // Output: [3, 2, 3]


~~~



The `arrayReplace` function is designed to search through an array and replace every occurrence of a specific element with a new one. This is useful when you want to transform an array without creating a completely new one or when you need to change specific values dynamically.

The function takes three arguments. The first argument, `inputArray`, is the original array of values. The second argument, `elemToReplace`, is the specific value we want to find and replace. The third argument, `substitutionElem`, is the new value that should replace the matched ones.

Inside the function, we use the `forEach()` method to loop over each element in the array. The `forEach()` method provides both the current element and its index. For every iteration, we check whether the current element is equal to `elemToReplace`. If it is, we update the value at that index in the original array with `substitutionElem`.

After the loop finishes, we return the modified array. This approach updates the original array in place and doesn’t create a new one. This is efficient and ideal for many simple array replacement tasks.

Here's an example usage of the function:

```javascript
console.log(arrayReplace([1, 2, 1], 1, 3)); 
In this example, we pass in the array [1, 2, 1] and ask the function to replace all occurrences of 1 with 3. The final result is [3, 2, 3], which is printed to the console.

This function is an elegant and straightforward solution for replacing items in an array based on a matching condition.


