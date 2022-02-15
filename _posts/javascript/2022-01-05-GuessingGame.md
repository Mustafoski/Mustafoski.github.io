---
layout: post
title: "Guessing Game"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-01-05T15:39:55-04:00
modified: 2022-01-05T15:39:55-04:00
---

## Guessing Game
Guessing Game is a game where you guess if the number from first function is the guess from the second one and if your guess is bigger you return "Your guess is too high!" else 
"Your guess is too low!"

Example:<br>
console.log(guessingGame(2)(5)); "You got it!"  <br>
console.log(guessingGame(2)(4)); "Your guess is too high!"<br>
console.log(guessingGame(2)(3)); "Your guess is too low!"<br>





~~~
function guessingGame(amount){
    var answer = Math.floor(Math.random()*11);
    var guesses = 0;
    var completed = false;
    return function(guess){
        if(!completed){
            guesses++
            if(guess === answer) {
                completed = true;
                return "You got it!"
            }
            else if(guesses === amount) {
                completed = true;
                return "No more guesses the answer was " + answer;
            }
            else if(guess > answer) return "Your guess is too high!"
            else if(guess < answer) return "Your guess is too low!"
        }
        return "You are all done playing!"
    }
}

console.log(guessingGame(2)(5)); "You got it!" 
console.log(guessingGame(2)(4)); "Your guess is too high!"
console.log(guessingGame(2)(3)); "Your guess is too low!"
~~~
___
We create a function called guessingGame with parameter called *amount* and *answer* to be Math.floor(Math.random() *11); We alse created *guesses* that start at 0 and *completed* to start at false; 
<br><br>
We return callback function with parameter *guess* and check if(*!completed*) so if it is not completed we increment the guesses with guesss ++
<br><br>
If *guess* == *answer* then we make *completed* = true and return "You got it"
<br><br>
Else if  guesses === amount we turn *completed*=true and return "No more guesses and answer was " + *answer*
<br><br>
Else if guess > answer we return "Your guess is too high!" 
<br><br>
Else if guess < answer we return "Your guess is too low!"
<br><br>
Else we return "You are all done playing!"
<br><br>