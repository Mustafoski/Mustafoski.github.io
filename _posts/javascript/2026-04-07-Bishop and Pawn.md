---
layout: post
title: "Bishop and Pawn"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2026-04-07T15:39:55-04:00
modified: 2026-04-07T15:39:55-04:00
---



# Bishop and Pawn

## Definition
--- **The "Bishop and Pawn" algorithm is a classic programming exercise (popular on platforms like CodeSignal or GeeksforGeeks) designed to test your understanding of coordinate geometry on a 2D grid.It boils down to one simple question: "Can a Bishop at $(x_1, y_1)$ capture a Pawn at $(x_2, y_2)$ in exactly one move?"**



---

~~~
const bishopAndPawn = function (bishop, pawn) {
  const board = {
    a:1,b:2,c:3,d:4,e:5,f:6,g:7,h:8
  };

  const bishopX = board[bishop[0]];
  const bishopY = parseInt(bishop[1]);

  const pawnX = board[pawn[0]];
  const pawnY = parseInt(pawn[1]);

  if (
    bishopX + bishopY === pawnX + pawnY ||
    bishopX - bishopY === pawnX - pawnY
  ) {
    return true;
  }

  return false;
};


~~~





### How It Works

1. ## 🏁 Summary


## ♟️ How It Works

### 1. Board Mapping


const board = {
  "a":1, "b":2, "c":3, "d":4,
  "e":5, "f":6, "g":7, "h":8
};


* Converts chess columns (`a–h`) into numeric values (`1–8`).



### 2. Extract Coordinates

#### Bishop


const bishopX = board[bishop[0]];
const bishopY = parseInt(bishop[1]);


#### Pawn


const pawnX = board[pawn[0]];
const pawnY = parseInt[pawn[1]];


* Splits positions like `"c1"` into:

  * X (column)
  * Y (row)



### 3. Capture Logic

####
if (
  bishopX + bishopY === pawnX + pawnY ||
  bishopX + pawnY === pawnX + bishopY
)


* A bishop moves diagonally.
* Two squares are on the same diagonal if:

  * Their **sum is equal**, OR
  * Their **difference is equal** (represented here using rearranged sums)



### 4. Return Result


return true;  // if capture possible
return 

---
