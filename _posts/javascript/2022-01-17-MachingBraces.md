---
layout: post
title: "Maching Braces"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-01-17T15:39:55-04:00
modified: 2022-01-17T15:39:55-04:00
---

## Maching Braces


Given an expression string exp, write a program to examine whether the pairs and the orders of “{“, “}”, “(“, “)”, “[“, “]” are correct in exp. The function is expected to return a String Array YES NO
<br>
Example:<br>
console.log(Brackets(["()[]()[]{}","([{}])", "()]]"]) [YES,YES,NO] <br>



~~~
function checkBraces(braces) {
    if (braces.length % 2 !== 0) return false;
    
    let i = 0;
    let result = [];
    while(i < braces.length) {
        if(braces[i] === "{" || braces[i] === "(" || braces[i]=== "[") {
           result.push(braces[i]);
        } else if(braces[i] === "}" && result[result.length-1] === "{") {
            result.pop()
        } else if(braces[i] === ")" && result[result.length-1] === "(") {
            result.pop()
        } else if(braces[i] === "]" && result[result.length-1] === "[") {
            result.pop()
        } else {
            return false;
        }
        i++
    }
    
    return result.length === 0;
};

function matchingBraces(braces) {
    let result = []
    braces.forEach((b) => {
        if (checkBraces(b)) result.push('YES');
        else result.push('NO');
    });
    
    return result;
}

~~~
___

First we create function in our case checkBraces with only one parameter named *braces*, also we create a *i* variable that will be equal to 0 and *result* to [] 
<br><br>
We check if (braces.length % 2 !== 0) return false;
<br><br>
We do while loop while i < braces.length and we do the following conditions:
<br><br>
 if(braces[i] === "{" || braces[i] === "(" || braces[i]=== "[") {
           *result*.push(braces[i]);<br>
We check if braces is { or ( or [ and if it is we push it into the *result* array.<br>
<br><br>
else if(braces[i] === "}" && result[result.length-1] === "{") {
            *result*.pop()<br>
We check if the braces is } and previous one is { than we have result true;<br>
<br><br>
else if(braces[i] === ")" && result[result.length-1] === "(") {
            *result*.pop()<br>
We check if the braces is ) and previous one is ( than we have result true;<br>
<br><br>
else if(braces[i] === "]" && result[result.length-1] === "[") {
            *result*.pop()<br>
Finally we check if braces is ] and previous one is [  than yet again we have result true;<br>
<br><br>
if none of these statements are true we return with else false; and increment i by 1;<br>
<br><br>
At the end if all the braces are removed we check  return *result*.length === 0;
<br><br>
We create another function called matchingBraces with parameter *braces* and variable *result* initialized to empty array [];
<br><br>
We loop the braces with forEach loop and inside we check <br>
if (checkBraces(b)) result.push('YES');<br>
else result.push('NO');<br>
<br><br>
In the end we return the result