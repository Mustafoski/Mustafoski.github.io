---
layout: post
title: "Longest Words"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2020-10-07T15:39:55-04:00
modified: 2020-10-07T15:39:55-04:00
---

## Longest Words


Given a string, return a the lenght of the largest word or words! from a sentence.

Example:<br>
longestWords('I woke up early this today') = [ 'early', 'today' ]<br>
longestWords('I went to straight to the beach  ') = [ 'straight' ]<br>




~~~
function longestWords(str){
  let words = str.split(' ');
  let size = 0;
  let max = [''];

  for(let i=0;i<words.length;i++){
    if(words[i].length >= size){
      size = words[i].length;
      if(max[max.length-1].length <words[i].length){
        max= [];
        max.push(words[i])
      }else {
        max = [...max,words[i]]
      }
    }
  }
  return [...max]
}

console.log(longestWords('I woke up early this today'));
console.log(longestWords('I went to straight to the beach  '))

~~~
___

We start working with making an array so we split the variable word into an array with words.split(' ') Hint: with a space between. We create initial size of 0 with let size = 0, and an empty array with empty string inside with max = ['']; <br>

Then we loop with traditional for loop. we start from zero to i to be less than words.length and we incremenet by 1.
Then we start checking the lenght the items we have in our array. And the way we do this is we check if the lenght of the word is bigger than the size; 
<br>

So we use  if(words[i].length >= size) we use bigger or equal because we might have two words the same length. Then we use size of variable equal to words[i].length.
<br>
So we check if (max[max.length-1].length (because array start from 0 index base) < words[i].length) This means that we are going to look for the max array and the last item in the max array and we check for the length then we are looking the words the items we are getting from the array is bigger than the last item we have in the initial array (in our case is empty string which means 0) then we make our array empty like this max = [];
<br>
Then we use the push method and we say we push(words[i])
<br>
Then we have else method from the if statement and that will be the array max and we use spread operator max = [...max, words[i]] which spells give me all the items you have in the max array and just add whatever item is in the words[i] array.
<br>
Last but not least we return the new array return [...max] 
