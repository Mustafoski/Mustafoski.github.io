---
layout: post
title: "Sieve of Eratosthenes"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-10-24T15:39:55-04:00
modified: 2021-10-24T15:39:55-04:00
---

## Sieve of Eratosthenes

In mathematics, the sieve of Eratosthenes is an ancient algorithm for finding all prime numbers up to any given limit.

Example:<br>
SieveOfEratosthenes(20); 
[
   2,  3,  5,  7,
  11, 13, 17, 19
] <br>




~~~

function SieveOfEratosthenes(num) {
  let primes = [];
  for (let i = 0; i <= num; i++) {
    primes[i] = true;
  }
  primes[0] = false;
  primes[1] = false;

  for (let i = 2; i <= Math.sqrt(num); i++) {
    for (let j = 2; j * i <= num; j++){
      primes[i * j ] = false;
    }
  }
  let result = [];
  for (let i = 0; i < primes.length;i++){
    if(primes[i]) result.push(i)
  }
  return result
}
SieveOfEratosthenes(20);
~~~
___

We create a function SieveOfEratosthenes with parameter of num in our case we return all prime numbers up to num in the array<br>

We create an array called *primes* that holds empty array.<br>
We use for loop to go through all the elements until *num* and then we assign primes[i] = true so all the values from the iteration are true <br>

Since we know 0 and 1 are not prime numbers we assign primes[0] = false and primes[1] = false <br>

We create another for loop that starts from 2 and it goes where i <= Math.sqrt(num) and i++. Math.sqrt is build in function in JavaScript.<br>

Inside this loop we create another for loop which we start again at 2 then we check j * i <= num and increase j in every iteration. We say while j * i is less or equal than the num because i * j because i * j is each multiple of the current index. <br>

For example outer loop is on second iteration so variable i is currently equal to 3. Our j variable starts at 2 so our first multiple is 6. On the next iteration i will still be 3 and j is going to be 3 so our multiple will be 9. And again in the next iterable i will be still 3 and j will be 4 so out multiple will be 12. We want to increase our multiples as long as it less than num.<br>

Inside our inner loop we will simple mark each multiples as false as we know all multiples are i * j with *primes[i * j] = false*; <br>


All we need to do is return the numbers that are prime and still marked as true. We will do this with another for loop but first we will create variable result = []<br>

Then we will write i = 0; i< primes.length;i++, Then we check with if statement if (primes[i]) are true we do result.push(i). push is another build in JavaScript function for adding into an array.
<br>

Finally we want to return the result array with result array;

