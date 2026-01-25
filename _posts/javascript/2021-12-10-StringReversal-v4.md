---
layout: post
title: "String Reversal v4"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-12-10T15:39:55-04:00
modified: 2021-12-10T15:39:55-04:00
---

## String Reversal v4

Given a string, return a new string with the reversed order of characters.

Example:<br>
reverse('apple') = 'leppa'<br>
reverse('hello') = 'olleh'<br>
reverse('Greetings') = 'sgniteerG'<br>

~~~
function reverse(str) {
 return str.split('').reduce((character, reversed) => {
    return character + reversed
  }, '')
}

console.log(reverse('apple')) => 'leppa'
~~~

We create a function in our case called reverse with a parameter I choose *str* 
<br><br>
Then we are going to return *str* parameter and use split method to turn the string into an array like *str.split('')*
<br><br>
Then we are going to chain reduce method that takes two arguments one callback function and second one starting initial value for our function which I'm going to pass in an empty string
<br><br>
This reduce function will run for one time for every element whitin the array so we can picture that this first value for the first argument that has passed in reduce is reduce string named *reversed*
<br><br>
And the second argument is the element of the character that we are currently operating on out of our array and we will call this second argument *character* 
<br><br>
The logic inside this function will be that we will take our *character* that we are operating right now we will add it to the total reverse string or the strng that represents the reversed string that we were past and then return the result.
<br>
return *character* + *reversed*