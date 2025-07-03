---
layout: post
title: "Reverse Array in Place"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2020-10-15T15:39:55-04:00
modified: 2020-10-15T15:39:55-04:00
---

## Reverse Array in Place

Reverse Array in Place this algorithm will take an array as a parameter and it will return to us the reversed array.
___

> ##For Example<br>
  [2,4,5,6,7,22,45] => [45, 22, 7, 6, 5,  4, 2]<br>
  [1,2,4,34,22] => [ 22, 34, 4, 2, 1 ]<br>
>
##
<br>

___

~~~

function reverseArrayInPlace(arr){
  for(let i = 0; i < arr.length / 2; i++){
    let tempVar = arr[i];
    arr[i] = arr[arr.length - 1 - i];
    arr[arr.length - 1 - i] = tempVar;
  }

  return arr;
}

console.log(reverseArrayInPlace(arr))
~~~

function reverseArrayInPlace(arr) { <br><br>

First we create a function called reverseArrayInPlace and pass an argument array called arr.

<br><br>
for(let i = 0; i < arr.length; i++){ <br>
    let tempVar = arr[i]; <br>
    arr[i] = arr[arr.length - 1 - i]; <br>
    arr[arr.length - 1 - i] = tempVar; <br>
  }<br>

<br><br> 

First thing that will be doing is writing a for loop to iterate through our array with. We will say for let a is equal to zero while i is less than arr.lenght and increment by one with i++.
What we want to do is switch the first element of our array with the last element of our array. We want to switch the second element of our array with the second to last element of the array and so on.

We will do this with temporary variable in our case tempVar, where we shall say variable tempVar is equal to arr[i] at position i. We now have the arr[i] value stored in tempVar.

Now we want to set the element of array array equal to its counterpart.
So we say arr[i] at position i equals to arr[arr.length - 1 - i] which is the last element of our array.

Then we want to write the counterpart to be equal to our tempVar that has the value of array of the position i.


<br><br>

return arr;

 
<br><br>

Now these seems that it will work correctly but it actually won't. 

This is because we are looping throuh the whole array in this for loop so as we go through the first half  of the array we are correctly reassigning each element but then as we continue through the second half of the array we are switching every element back again.


<br><br>

for(let i = 0; i < arr.length / 2; i++){<br>

<br><br>

We can fix this by only looping through the first half of the array so we will change this for loop to say while i is less than array. length dividing by 2 (by half)

<br><br>

