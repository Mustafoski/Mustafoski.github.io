---
layout: post
title: "Array Chunk v2"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-12-24T15:39:55-04:00
modified: 2021-12-24T15:39:55-04:00
---

## Array Chunk v2


Given an array of chunk size, divide the array into many subarrays where each subarray is of length size.

Example:<br>
console.log(chunk([1,2,3,4],2)); => [[1, 2], [3, 4]] <br>
console.log(chunk([1,2,3,4,5],10)) => [[1, 2, 3, 4, 5]] <br>
console.log(chunk([1,2,3,4,5,6,7,8],3)); => [[1, 2, 3], [4, 5, 6], [7, 8]] <br>
console.log(chunk([1,2,3,4,5],2)); = > [[1, 2], [3, 4], [5]] <br>





~~~
function chunk(array, size) {
  const chunked = [];
  let index = 0;

  while (index < array.length) {
    chunked.push(array.slice(index, index + size));
    index += size;
  }
  return chunked;
}

console.log(chunk([1,2,3,4],2));
console.log(chunk([1,2,3,4,5],10))
console.log(chunk([1,2,3,4,5,6,7,8],3)); 
console.log(chunk([1,2,3,4,5],2))

}
~~~

First we create a function chunk with 2 parameters *array* and *size* and first we will declare a new array that is going to hold all these different chunks named *chunked = []* and *index = 0*
<br><br>
Next we will loop with while loop where index is less thant array.length
<br><br>
First we will write slice statement. So we want to slice everything from index to index + size. Array that slice produces an array that contains some number of elements out of the original array.  
<br><br>
So we can take this slice that gets produced and just stick it directly into the chunked array by using the push method; by writing chunked.push(array.slice(index, index + size))
<br><br>
Then immediately after that after we do our slice statement right here we need to move on to the next index. So we are going to take our index variable and we'll add size to it
<br><br>
So we are not incrementing by one here we are incrementing by the size variable because we want essentially take big scoops out of the original array over time
<br><br>
So we say index plus equal size and then remember that one very important step that i would never want you'll for get makes sure you return *chunked* at the bottom.