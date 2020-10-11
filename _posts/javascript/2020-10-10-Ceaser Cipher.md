---
layout: post
title: "Caeser Cipher"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2020-10-09T15:39:55-04:00
modified: 2020-10-09T15:39:55-04:00
---

## Caeser Cipher

Caeser Cipher is shifting every letter by any number passed in.
___

> ##For Example
  finction caeserCipher(str,num )zoo keeper => num(2) (str)zoo keeper =>bqq mggrgt

>
##
<br>

___

~~~
function caesarCipher(str,num) {
  num = num % 26;
  var lowerCaseString = str.toLowerCase();
  var alphabet = 'abcdefghijklmnopqrstuvwxyz'.split('');
  var newString = '';
  
  for (var i = 0; i < lowerCaseString.length; i++) {
    var currentLetter = lowerCaseString[i];
    if (currentLetter === ' ') {
      newString += currentLetter;
      continue;
    }
    var currentIndex = alphabet.indexOf(currentLetter);
    var newIndex = currentIndex + num;
    if (newIndex > 25) newIndex = newIndex - 26;
    if (newIndex < 0) newIndex = 26 + newIndex;
    if (str[i] === str[i].toUpperCase()) {
      newString += alphabet[newIndex].toUpperCase();
    }
    else newString += alphabet[newIndex];
  };
  
  return newString;
}
caesarCipher('Zoo Keeper', 2); 

~~~

function caesarCipher(str,num) { { <br><br>
First we create a function called caesarCipher and pass an arguments called str and num.<br><br>
var lowerCaseString = str.toLowerCase();
  });<br><br>
We say variable lowerCaseString is equal str.toLowerCase() method turning all strings into a lowercase.<br><br>
    var alphabet = 'abcdefghijklmnopqrstuvwxyz'.split('');
  });<br><br>
  Then we say variable alphabet variable tp every letter in the alphabet and then use split method to turn the string into an array of single letters
<br><br>
for (var i = 0; i < lowerCaseString.length; i++) {
    var currentLetter = lowerCaseString[i];
    if (currentLetter === ' ') {
      newString += currentLetter;
      continue;
    } <br><br>
We loop into every letter with for loop where we start from 0 then i is lower than lowerCaseString and increment by one. Also we create new variable var newString = ''; that equals to empty string. 
so we say variable currentLetter = lowerCaseString[i] at position i.

We check if that position is space character.
So we check with if statement if currentLetter is equal to space. if true we use newString += currentLetter; At the end of this part we use continue. That says skip whatever is left of this functionality and move to the other staff.<br><br>
var currentIndex = alphabet.indexOf(currentLetter);
    var newIndex = currentIndex + num;
    if (newIndex > 25) newIndex = newIndex - 26;
    if (newIndex < 0) newIndex = 26 + newIndex;
    if (str[i] === str[i].toUpperCase()) {
      newString += alphabet[newIndex].toUpperCase();
    }
    else newString += alphabet[newIndex];
  };.<br><br>

The next thing is to find where our current letter is in our alphabet.
So we say var currentIndex is equal to alhabet with the method indexOf current index.
Then we say varibale newIndex is equal to currentIndex  + num; This is the index of our current array.
If our index is greater than 25 we check with if statement to make sure it loops to one again.
We check if newIndex > 25 our new index is equal to newIndex -26 which is the lenght of our alphabet array.<br><br>

If our newIndex is smaller than 0 we say newIndex = 26 + newIndex; which essentually wraps the letter back around to the end of the alphabet.
Finally we say newString  += to alphabet[newIndex] which is our newly shifted letter.
<br><br>
  if (str[i] === str[i].toUpperCase()) {
      newString += alphabet[newIndex].toUpperCase()
      else newString += alphabet[newIndex];
      <br><br>

Now we check for few things for example what if one or more of our letters in the original string is uppercase. We want that letter to be uppercase in our new letters.

We check if str[i] is equal to str[i].toUpperCase() we use newString and concat with alphabet of position newIndex and use toUpperCase() method in javascript. if true we create an else statement that says newString is concat with alphabet of index newIndex.  num = num % 26;  <br><br>

  num = num % 26;

We basically want to keep looping through the alphabet  until we have shifted the letter forward times a simple way to achieve this functionality without actually looping through the alhabet without actually looping through the alphabet a bunch of times is to use the modulus operator.
So we write our original number num is equal num modulus 26 which is the lenght of alhabet. <br><br>

return newString;
}
caesarCipher('Zoo Keeper', 2);<br><br>

At the end we return the newString.