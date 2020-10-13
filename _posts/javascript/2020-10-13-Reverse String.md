---
layout: post
title: "Reversed String-v3"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2020-10-12T15:39:55-04:00
modified: 2020-10-12T15:39:55-04:00
---

## Reversed String

Reversed String is when we reverse a string or a word in a sentence and then return the whole string with reversed letters.
___

> ##For Example<br>
  'this is a string of words' => 'sith si a gnirts fo sdrow'<br>
  'Coding JavaScript' => 'gnidoC trircsavaJ'<br>
>
##
<br>

___

~~~

function reverseWords(str){
  var wordsArr = str.split(' ');
  var reversedWordsArr = [];

  wordsArr.forEach(word) {
    let reversedWord = '';

    for(var i = word.length - 1; i >= 0; i--){
      reversedWord += word[i];
    }
    reversedWordsArr.push(reversedWord);
  }
  return reversedWordsArr.join(' ');
}

~~~

function reverseWords(str) { <br><br>
First we create a function called uniqueValues and pass an argument called string.<br><br>
var wordsArr = str.split(' ')<br><br> 

The first thing we have to do is to create an array to hold all the strings. So we create the variable wordsArr and we split with space to hold all the strings
<br><br>

var reversedWordsArr = [];
 
<br><br>

We then have to define an empty array to push all of our reversed words each of them. So we create a variable var reversedWordsArr = [];

<br><br>

wordsArr.forEach (word => {<br>
  var reversedWord = '';  <br>
})<br>
<br><br>
We now want to loop to every word in our words array and we will do this with the forEach loop and we need to reverse our every words in our wordsArr.<br>
The first thing we want to do is to find an empty string to build our reversed string. that is our new variable var reversedWord = ''; 

<br><br>
for(var i = word.length - 1; i >= 0; i--){ <br>
  reversedWord += word[i];    <br>
}<br>
  reversedWordsArr.push(reversedWord);<br>
<br><br>

Now we want to loop throught every letter in our word backwards and added to the empty string that is our reversedWords variable. We will loop with the for loop so we will say for variable i equals words.length minus one while i is bigger or equal to 0 and i -- we decrement by one.Then we use our reversedWord and add each word with the parameter of i. Then outside of the for loop but inside the forEach loop we use our empty array reversedWordsArr to push every reversedWord with the push method.
<br><br>

return reversedWordsArr.join (' ')

<br><br>

At the end we return the reversedWordsArr joined with the join method and space between the quotes.

<br

