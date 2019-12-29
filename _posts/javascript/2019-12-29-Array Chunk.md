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
date: 2019-12-29T15:39:55-04:00
modified: 2019-12-29T15:39:55-04:00
---

## Array Chunk


Given an array of chunk size, divide the array into many subarrays where each subarray is of length size.

Example:<br>
chunk([1,2,3,4],2) = [[1,2],[3,4]]<br>
chunk([1,2,3,4,5],2) = [[1,2],[3,4],[5]]<br>
chunk([1,2,3,4,5,6,7,8],3) = [[1,2,3],[4,5,6],[7,8,]]<br>
chunk([1,2,3,4,5],4) = [[1,2,3,4],[5]<br>
chunk([1,2,3,4,5],10) = [[1,2,3,4,5]]<br>
<br>



~~~
function chunk(array, size) {
	const cunked = [];

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
~~~
___

We create empty array to hold chunks called chunked
For each element in the unchuncked array
Retreive the last element in chuncked
If last element does not exist, or if its lenght is equal to chunk size.
Then push a new chunk into chunked with the current element
else add the current element into the chunk