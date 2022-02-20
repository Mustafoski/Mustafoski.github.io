---
layout: post
title: "Spiral Matrix v-1"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-01-24T15:39:55-04:00
modified: 2022-01-24T15:39:55-04:00
---

## Spiral Matrix v-1
Write a function that accepts an integer N and returns a NxN spiral matrix.'


Example:<br>
matrix(2)<br>
    [[1, 2],<br>
     [4, 3]]<br>
   matrix(3)<br>
     [[1, 2, 3],<br>
     [8, 9, 4],<br>
     [7, 6, 5]]<br>
   matrix(4)<br>
     [[1,   2,  3, 4],<br>
     [12, 13, 14, 5],<br>
     [11, 16, 15, 6],<br>
     [10,  9,  8, 7]]<br>





~~~
function matrix(n) {
  const results = [];
  for (let i = 0; i < n; i++) {
    results.push([]);
  }

  let counter = 1;
  let startColumn = 0;
  let endColumn = n - 1;
  let startRow = 0;
  let endRow = n - 1;

  while (startColumn <= endColumn && startRow <= endRow) {
    // TOP row
    for (let i = startColumn; i <= endColumn; i++) {
      results[startRow][i] = counter;
      counter++;
    }
    startRow++;

    // Right Column
    for (let i = startRow; i <= endRow; i++) {
      results[i][endColumn] = counter;
      counter++;
    }
    endColumn--;

    // Bottom Row
    for (let i = endColumn; i >= startColumn; i--) {
      results[endRow][i] = counter;
      counter++;
    }
    endRow--;

    // start column
    for (let i = endRow; i >= startRow; i--) {
      results[i][startColumn] = counter;
      counter++;
    }
    startColumn++;
  }
  return results;
}
~~~
___
We create a function called matrix with parameter called *n* and variable called *results*=[] 
<br><br>
We start looping with for loop for all the numbers and if found it is used .push to push into the *results* array
<br><br>
We create 5 variable to keep track with our rows and columns<br>
  let counter = 1;<br>
  let startColumn = 0;<br>
  let endColumn = n - 1;<br>
  let startRow = 0;<br>
  let endRow = n - 1;<br>
<br>
Then we use the while loop like this ***while (startColumn <= endColumn && startRow <= endRow)***
<br><br>
First we check the TOP ROW and we create for loop where *i* = *startColumn* and is less than *endColumn* and also we increment by 1;
<br><br>
Inside the loop we check results of startRow and *i* and equal to counter then we increment     *counter* by 1; after that we increment *startRow* by 1 with *startRow*++
***results[startRow][i] = counter; <br>
      counter++;
    }
    startRow++;***
<br><br>
Then we check the Righ Column and we create for loop where *i* = *startRow* *i*<= *endRow* and *i*++<br>
  ***results[i][endColumn] = counter;
      counter++;
    }
    endColumn--;***
<br><br>
Then we check the Bottom Row and we create for loop where *i* = *endColumn* *i*>= *startRow* and *i*-- <br>
   ***results[endRow][i] = counter;
      counter++;
    }
    endRow--;***
  <br><br>
  Then we check the Start Column and we create for loop where *i* = *endRow* *i*>= *startRow* and *i*-- <br>
      ***results[i][startColumn] = counter;
      counter++;
    }
    startColumn++;***

<br><br>
In the end we return the *results* 

  