---
layout: post
title: "LinkedList"
comments: true
share: true
modified:
categories: algorithms
excerpt:
tags: []
image:
  feature:
date: 2021-01-07T15:39:55-04:00
modified: 2021-01-07T15:39:55-04:00
---

## LinkedList
SLinkedList is data structure that is good for lists.

___

##For Example<br>
console.log(myLinkedList)=> LinkedList {
							head:{value:10,next:null<br>
							Tail:{value:10,next:null}
							length:1 }



<br>


___

~~~

class LinkedList {
  constructor(value) {
    this.head = {
      value: value,
      next: null
    };
    this.tail = this.head;
    this.length = 1;
  }
  append(value) {
    //Code here
  }
}

let myLinkedList = new LinkedList(10);

console.log(myLinkedList)



~~~

We create class LinkedList { and constructor(value)<br><br>

constructor has only one parameter value and inside the constructor we have 
this.head = { value:value and next:null}

<br><br>

Outside of the constructor we have this.tail = this.head pointing to the class Linked List
<br><br>
this.length is optional to check where we are and we assign to 1


<br><br>
	
const myLinkedList = new LinkedList(10) we instaciate new object and we put parameter to where to start, in our case 10.

<br><br> 



<br><br> 