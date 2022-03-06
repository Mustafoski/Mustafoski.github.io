---
layout: post
title: "Queue Stack"
comments: true
share: true
modified:
categories: algorithms
excerpt:
tags: []
image:
  feature:
date: 2022-03-05T15:39:55-04:00
modified: 2022-03-05T15:39:55-04:00
---

## Queue Stack

Implement a Queue datastructure using two stacks. **Do not** create an array inside of the 'Queue' class. Queue should implement the methods 'add', 'remove', and 'peek'.
For a reminder on what each method does, look back at the Queue exercise.
--- Examples<br>
    const q = new Queue();<br>
    q.add(1);<br>
    q.add(2);<br>
    q.peek();  // returns 1<br>
    q.remove(); // returns 1<br>
    q.remove(); // returns 2<br>
Example:<br>
console.log(PassingCars([0,1,0,1,1])); -> 5<br>




~~~
class Stack {
  constructor() {
    this.data = [];
  }

  push(record) {
    this.data.push(record);
  }

  pop() {
    return this.data.pop();
  }

  peek() {
    return this.data[this.data.length - 1];
  }
}

module.exports = Stack;
****************************************************************************************************
const Stack = require('./stack');

class Queue {
  constructor() {
    this.first = new Stack();
    this.second = new Stack();
  }

  add(record) {
    this.first.push(record);
  }
  remove() {
    while (this.first.peek()) {
      this.second.push(this.first.pop());
    }
    const record = this.second.pop();
    while (this.second.peek()) {
      this.first.push(this.second.pop());
    }
    return record;
  }

  peek() {
    while (this.first.peek()) {
      this.second.push(this.first.pop());
    }
    const record = this.second.peek();

    while (this.second.peek()) {
      this.first.push(this.second.pop());
    }
    return record;
  }
}

module.exports = Queue;


~~~
___
First we create a class Stack and a field **data = []**
<br><br>
First method in the Stack class is **add** so we ***add(record) {
    this.data.push(record);<br>***
  }<br>
Second method in the Stack class is **pop** so we <br>
  ***pop() {<br>
    return this.data.pop();<br>
  }***<br>
The last method in the Stack class is **peek** so we <br>
  ***peek() {<br>
    return this.data[this.data.length - 1];<br>
  }***<br>
In the end we module.exports = Stack;
<br><br>

First we recive the Stack class like this ***const Stack = require('./stack');***
<br><br>
We create a class called **Queue** and initilized two fields  
***this.first = new Stack();<br>
  this.second = new Stack();***<br>
<br><br>
We start with the add method ***add(record) {<br>
    this.first.push(record);<br>
  }***<br>
<br><br>
Then we go to the second method **Remove** ***remove() {
    while (this.first.peek()) {
      this.second.push(this.first.pop());
    }
    const record = this.second.pop();
    while (this.second.peek()) {
      this.first.push(this.second.pop());
    }
    return record;
  }***
  <br><br>
  We loop with while loop until the last item in the array is there that is what peek is doing <br>
  If there is an space in the first array we push second to the end of first array and we pop the <br>last item of the first array. In simple terms we swich **this.second** to be the last in **<br>this.first*** by using push and pop JavaScript methods.<br><br>
  Then we create a **const record variable** that is equal to second.pop() the item we just retrieved. And ***while(this.second.peek()){
    this.first.push(this.second.pop());
  }
  return record***
  <br><br>
  So we do the same thing only this time we take from second with pop method and that we push it to first. In the end I return **record**;
<br> <br> 
Last method is peek method <br>
***peek() {<br>
    while (this.first.peek()) {<br>
      this.second.push(this.first.pop());<br>
    }<br><br>
    const record = this.second.peek();<br>
    while (this.second.peek()) {<br>
      this.first.push(this.second.pop());<br>
    }<br>
    return record;<br>
  }<br>
}***<br>
<br><Br>
First we do a while loop to see if there is a remaining item and if there is we use like in remove<br> above we take last item with pop() from first field and we push it to the second field with push()<br>
Then we create a **const record variable** that is equal to second.peek(). <br>
And ***while(this.second.peek()){<br>
    this.first.push(this.second.pop());<br><br>
  }<br>
  return record***
  <br><br>
While this.second.peek() so it checks if there is a variable and if there is it takes from second field with pop() and added with push() to the first.<br><br>

In the end ***return record*** and **module.exports = Queue;**
 

