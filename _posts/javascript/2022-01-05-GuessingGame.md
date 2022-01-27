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
We create a function called specialMultiply with parameter called *a* and *b* 
<br><br>
We check if (arguments.length ===1) {} 
<br><br>
If true we return another function with parameter *b* and return a*b
<br><br>
In the end we return again a*b
<br><br>
