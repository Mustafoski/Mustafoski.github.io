---
layout: post
title: "Rock Paper Scissors"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2019-12-30T15:39:55-04:00
modified: 2019-12-30T15:39:55-04:00
---

## Rock Paper Scissors


Mini app for rock paper scissors

~~~
<html>

<head>
    <title>JavaScript</title>
</head>

<body>
    <div class="score"></div>
    <div class="message"></div>
    <button type="button">Rock</button>
    <button type="button">Paper</button>
    <button type="button">Scissors</button>
~~~

~~~
const message = document.querySelector(".message");
        const score = document.querySelector(".score");
        const buttons = document.querySelectorAll("button");
        let winner = [0, 0];

        for (let i = 0; i < buttons.length; i++) {
            buttons[i].addEventListener("click", playGame);
        }

        function playGame(e) {
            let playerSelection = e.target.innerText;
            let computerSelection = Math.random();
            if (computerSelection < 0.34) {
                computerSelection = "Rock";
            }
            else if (computerSelection <= 0.67) {
                computerSelection = "Paper";
            }
            else {
                computerSelection = "Scissors";
            }
            let result = checkWinner(playerSelection, computerSelection);
            if (result == "Player") {
                result += " wins!";
                winner[0]++;
            }
            else if (result == "Computer") {
                result += " wins!";
                winner[1]++;
            }
            else {
                result += " results in a tie match";
            }
            score.innerHTML = "<small>Player</small>[" + winner[0] + "] <small>Computer</small>[" + winner[1] + "]";
            messager(playerSelection + " vs " + computerSelection + "<br><b>" + result + "</b>");
        }

        function messager(mes) {
            message.innerHTML = mes;
        }

        function checkWinner(pl, co) {
            if (pl === co) {
                return "Draw";
            }
            if (pl === "Rock") {
                if (co === "Paper") {
                    return "Computer";
                }
                else {
                    return "Player";
                }
            }
            if (pl === "Paper") {
                if (co === "Scissors") {
                    return "Computer";
                }
                else {
                    return "Player";
                }
            }
            if (pl === "Scissors") {
                if (co === "Rock") {
                    return "Computer";
                }
                else {
                    return "Player";
                }
            }
        }
~~~
___

First we build the html structure all the components we are going to need for the game play<br>
Next we selected all the elements and put it in the objects<br>
Next we initialized global array winner to keep track of winning<br>
We did event listener inside a for loop<br>
Next we choose 1/3 of each of Rock Paper Scissors <br>
We needed to see who won so we created a quick little function checkWinners and it is a combination of who selected what <br>
add a space to the level<br> 
console.log(level)<br>