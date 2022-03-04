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

Implement a Queue datastructure using two stacks. *Do not* create an array inside of the 'Queue' class. Queue should implement the methods 'add', 'remove', and 'peek'.
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
*****************************************************************************************************
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
We create a function called CarsPassing with parameter called *inputArray* we create an variable called *suffixSum* and it will be an array with size of *inputArray.length + 1* and initially we fill the array with 0. Next we create varible  *count* that we initialize to 0;
<br><br>
We create for loop where we start with *i* = *inputArray.length - 1*, second condition is *i* is bigger or equal to 0 and third condition is where we decrement i by 1;
<br><br>
The way we compute the *suffixSum* is to write *suffixSum[i] = inputArray[i] + suffixSum[i + 1];*
*suffixSum* one position more than i and i + 1 is the reason why we have created the suffixSum to be one position bigger than our inputs.
<br><br>
And in this way the suffix sum area is kindd of a table containing the numbers of cars that are still in front of us for each position.
<br><br>
Next we have if statement *if (inputArray[i] === 0) count += suffixSum[i]* Meaning that the car is traveling EAST we need to update the count variable with count += suffixSum[i]
<br><br>
Final thing we have to do is another if statement *if (count > 1000000000) return -1;* If the count is bigger than 1,000,000,000 we return -1;  
<br> <br> 
In the end we return count;
 

