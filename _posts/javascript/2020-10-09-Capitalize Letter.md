---
layout: post
title: "Capitalize Letter"
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

## Capitalize Letter

Capitalize Letter is when in a sentence every word has capitalize letter.

___
Given a sentence, return first letter capitalized
> ##For Example
  I got up early today => I Got Up Early Today
  I walked straight to the beach => I Walked Straight To The Beach
>
##
<br>

___

~~~
function capitalizeWords(string) {
  let words = string.split(' ').map(word => {
    return word.charAt(0).toUpperCase() + word.slice(1);
  });
    return words.join(' ')
}

capitalizeWords("I got up early today") 
capitalizeWords("I walked straight to the beach") 

~~~

function capitalizeWords(string) { <br><br>
First we create a function called capitalizeWords and pass an argument called string.<br><br>
let words = string.split(' ').map(word => {
    return word.charAt(0).toUpperCase() + word.slice(1);
  });<br>
We create a variable words and we split with space between like this part of the code string.split(' ') <br><br>
.map(word => {
    return word.charAt(0).toUpperCase() + word.slice(1);
  });<br><br>
Then we chain the map method and we say map this array made with split method and go to every word and word of charAt of 0 (first word) we chain toUpperCase() invoked to make the first letter capitalized and we concat with + operator to word.slice(1) which means concat the rest of the word from second to the rest that is why we write word.slice(1) 0 is first index 1 is one and rest.<br><br>
 return words.join(' ')
}
<br><br>
At the end we return the words but joined but since we splited with space inside quotes now we have to use space in the join method. <br><br>

capitalizeWords("I got up early today") returns I Got Up Early Today
capitalizeWords("I walked straight to the beach") returns I Walked Straight To The Beach
