---
layout: post
title: "Array Chunk"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-12-16T15:39:55-04:00
modified: 2021-12-16T15:39:55-04:00
---

## Array Chunk


Given an array of chunk size, divide the array into many subarrays where each subarray is of length size.

Example:<br>
console.log(chunk([1,2,3,4],2)) <br>
[[1], [2], [3], [4]]<br>
console.log(chunk([1,2,3,4,5],10))<br>
 [[1], [2], [3], [4], [5]]<br>
console.log(chunk([1,2,3,4,5,6,7,8],3)) <br>
[[1], [2], [3], [4], [5], [6], [7], [8]]<br>
console.log(chunk([1,2,3,4,5],2))<br>
[[1], [2], [3], [4], [5]]<br>
<br><br>





~~~
function chunk(array, size) {
	const chunked = [];

	for (let element of array) {
		const last = chunked[chunked.lenght -1];

		if(!last || last.lenght === size) {
			chunked.push([element]);
		}else {
			last.push(element)
		}
	}
	return chunked;
}

console.log(chunk([1,2,3,4],2)) 
[[1], [2], [3], [4]]
console.log(chunk([1,2,3,4,5],10))
 [[1], [2], [3], [4], [5]]
console.log(chunk([1,2,3,4,5,6,7,8],3)) 
[[1], [2], [3], [4], [5], [6], [7], [8]]
console.log(chunk([1,2,3,4,5],2))
[[1], [2], [3], [4], [5]]
~~~

First we create a function chunk with 2 parameters *array* and *size* and first we will declare a new array that is going to hold all these different chunks named *chunked = []* 
<br><br>
Next we will iterate through the original *array* with for of loop. Inside we do temporary variable *last* = chunked[chunked.length - 1];
<br><br>
Now we check if that last element does not exist or if its length is equal to chunk size because if it is we want to push a new chunk into *chuncked* with the current element that we are iterating<br><br>

Still inside the loop we check if (!last || last.length === *size*) if true we use the .push() JavaScript build in method to push in our case element. like chunked.push([element])

<br><br>
Lastly we need to take of is the case in which we already have a chunk but it is not yet full. So in that case we are going to take the current element and add it to the chunk and and the chunk in mind is *last*
<br><br>
Else last.push(element)
<br><br>
At the end we return chunked;