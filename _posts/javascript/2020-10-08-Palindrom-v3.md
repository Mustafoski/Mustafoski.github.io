---
layout: post
title: "Palindrom-v3"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2020-10-08T15:39:55-04:00
modified: 2020-10-08T15:39:55-04:00
---

## Palindrom

A palindrome is a word, number, phrase, or other sequence of characters which reads the same backward as forward, such as ‘’taco cat’’ or madam or racecar or the number 10801

___
Given a string, return true if the string is a palindrome or false if it is not.

> ##For Example
const test3 = Emir<br>
const test4 = Palindrom<br>
Should return false<br>
const test = Anna<br>
const test2 =Racecar<br>
Should return true<br>
##
<br>

___

~~~
function isPalindrom(string) {
  string = string.toLowerCase();
  let charactersArray = string.split('');
  let validCharacters = 'abcdefghijklmnopqrstuvwxyz'.split('');

  let lettersArray = [];
  charactersArray.forEach(character => {
    if(validCharacters.indexOf(character) > -1 )
    lettersArray.push(character)
  })
  if(lettersArray.join('') === lettersArray.reverse().join('')){
  return true
  }else {
    return false
  }
}

isPalindrom("Madam I'm Adam") 
~~~

function isPalindrom(string) { <br>
First we create a function called isPalindrom and pass an argument called string.<br>
string = string.toLowerCase();<br>
To be concise we turn our parameter string to lower case so it will be easier to check only lowercase characters <br>
let charactersArray = string.split('');<br>
We create variable charactersArray and use to split the parameter into an array of letters<br>
let validCharacters = 'abcdefghijklmnopqrstuvwxyz'.split(''); <br>
In order to be more safe we create variable validCharacters and pass all the letters from the alphabet into a string first then we split the alphabet into a array of alphabet letters. <br>
 let lettersArray = [];<br>
 We create an empty array called lettersArray to push in the future letters from another array <br>
 charactersArray.forEach(character => {
    if(validCharacters.indexOf(character) > -1 )
    lettersArray.push(character)
  })<br>
  We use forEach method to loop from the characters from the parameter of the function and we say loop from the character array and for each character check if the character is valid which means check if the character from the string parameter is validCharacter that is bigger than -1 and if it returns to be true push that character into the lettersArray array with the push method <br>
  if(lettersArray.join('') === lettersArray.reverse().join('')){
  return true
  }else {
    return false
  }
}<br>
Then we check if the lettersArray joined with the join method is equal to lettersArray reversed with the reverse method and then joined. If it is palindrom or if the letters are the same we return true if not we return false.
