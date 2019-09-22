---
layout: post
title: "How to solve problems"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2017-03-01T15:39:55-04:00
modified: 2017-03-01T15:39:55-04:00
---

## How to solve problems

In order to solve coding problems we need to learn at least these Data Structures:
	1. Array						5. Trees
	2. Stacks						6. Tries
	3. Queues						7. Graphs
	4. Linked List					10.Hash Table


Also we need to learn these Algorithms:

	1. Sorting
	2. Dynamic Programming
	3. BFS + DFS (Searching)
	4. Recursion

There are a lot more Data Structures and a lot more Algorithms.

##The 3 pillars of good code: 
1.Readable 
2.Time Complexity 
3.Space Complexity

##For Example
const array1 = ['a','b','c','x'];
const array2 = ['z','y','i'];
Should return false
const array1 = ['a','b','c','x'];
const array2 = ['z','y','x'];
Should return true
##

~~~
function containsCommonItem(arr1, arr2) {
	for (let i = 0; i<arr1.lenght;i++){
		for (let j = 0; j <arr2.lenght; j++){
			if(arr1[i] === arr2[j]){
				return true;
			}
		}
	}
	return false;
}

containsCommonItem(array1,array2);

~~~

First for loop a checks with z, y, x, also b c and x from array1 checks first z, y, x,