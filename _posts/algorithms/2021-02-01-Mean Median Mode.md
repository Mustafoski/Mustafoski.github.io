---
layout: post
title: "Mean Median Mode "
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-02-01T15:39:55-04:00
modified: 2021-02-01T15:39:55-04:00
---

## Mean Median Mode
The mean (average) of a data set is found by adding all numbers in the data set and then dividing by the number of values in the set. The median is the middle value when a data set is ordered from least to greatest. The mode is the number that occurs most often in a data set.
___


##Example
meanMedianMode([1,2,3,4,5,4,6,1]); => { mean: 3.25, median: 3.5, mode: [ '1', '4' ] } <br>
meanMedianMode([9,10,23,10,23,9]); => { mean: 14, median: 10, mode: [] }
<br>


___

~~~

function meanMedianMode(array) {
  return {
    mean: getMean(array),
    median: getMedian(array),
    mode: getMode(array)
  }
}

function getMean(array) {
  var sum = 0;
  
  array.forEach(num => {
    sum += num;
  });
  
  var mean = sum / array.length;
  return mean;
}

function getMedian(array) {
  array.sort(function(a, b){return a-b});
  var median;
  
  if (array.length % 2 !== 0) {
    median = array[Math.floor(array.length / 2)];
  }
  else {
    var mid1 = array[(array.length / 2) - 1];
    var mid2 = array[array.length / 2];
    median = (mid1 + mid2) / 2;
  }
  
  return median;
}

function getMode(array) {
  var modeObj = {};
  
  // create modeObj
  array.forEach(num => {
    if (!modeObj[num]) modeObj[num] = 0;
    modeObj[num]++;
  });
  
  // create array of mode/s 
  var maxFrequency = 0;
  var modes = [];
  for (var num in modeObj) {
    if (modeObj[num] > maxFrequency) {
      modes = [num];
      maxFrequency = modeObj[num];
    }
    else if (modeObj[num] === maxFrequency) modes.push(num);
  }
  // if every value appears same amount of times 
  if (modes.length === Object.keys(modeObj).length) modes = [];
  return modes;
}


meanMedianMode([9,10,23,10,23,9]);
;





~~~
We create a function meanMedianMode(array) also we define tree other function <br>
1. function getMean(array) <br>
2. function getMedian(array)<br>
3. function getMode(array)<br>

<br><br>
function meanMedianMode(array) {<br>
  return {<br>
    mean:getMean(array),<br>
    median:getMedian(array),<br>
    mode:getMode<br>
  }<br>
}<br>

<br><br>


function getMean(array) {<br> 
  var sum = 0;<br>
  
  array.forEach(num => {
    sum += num;

  });
  <br>
  var mean = sum / array.length;<br>
  return mean;<br>
}

<br><br>

function getMedian(array) {<br>
  array.sort(function(a, b){return a-b});<br>
  var median;<br>
  
  if (array.length % 2 !== 0) {
    median = array[Math.floor(array.length / 2)];
  }
  else {
    var mid1 = array[(array.length / 2) - 1];
    var mid2 = array[array.length / 2];
    median = (mid1 + mid2) / 2;
  }
  
  return median;
}<br>

<br><br>
<br>function getMode(array) {
  <br>var modeObj = {};
  
  // create modeObj
  array.forEach(num => {
    if (!modeObj[num]) modeObj[num] = 0;
    modeObj[num]++;
  });
  
  // create array of mode/s 
  var maxFrequency = 0;
  var modes = [];
  for (var num in modeObj) {
    if (modeObj[num] > maxFrequency) {
      modes = [num];
      maxFrequency = modeObj[num];
    }
    else if (modeObj[num] === maxFrequency) modes.push(num);
  }
  // if every value appears same amount of times 
  if (modes.length === Object.keys(modeObj).length) modes = [];
  return modes;
}

meanMedianMode([1,2,3,4,5,4,6,1]);