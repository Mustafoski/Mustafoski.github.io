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
date: 2019-09-22T15:39:55-04:00
modified: 2019-09-22T15:39:55-04:00
---

## How to solve problems

In order to solve coding problems we need to learn at least these Data Structures:<br>
	1. Array<br>						5. Trees<br>
	2. Stacks<br>						6. Tries<br>
	3. Queues<br>						7. Graphs<br>
	4. Linked List<br>					10.Hash Table<br>


Also we need to learn these Algorithms:

	1. Sorting
	2. Dynamic Programming
	3. BFS + DFS (Searching)
	4. Recursion

There are a lot more Data Structures and a lot more Algorithms.

The 3 pillars of good code: 
	1.Readable 
	2.Time Complexity 
	3.Space Complexity

##For Example
const array1 = ['a','b','c','x'];<br>
const array2 = ['z','y','i'];<br>
Should return false<br>


const array1 = ['a','b','c','x'];<br>
const array2 = ['z','y','x'];<br>
Should return true<br>
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

First for loop a checks with z, y, x
Also b c and x from array1 checks first z, y, x,