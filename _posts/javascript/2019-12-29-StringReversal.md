---
layout: post
title: "Reverse String-v2"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2019-12-29T15:39:55-04:00
modified: 2019-12-29T15:39:55-04:00
---

## Reverse String


Given a string, return a new string with the reversed order of characters.

Example:<br>
reverse('apple') = 'leppa'<br>
reverse('hello') = 'olleh'<br>
reverse('Greetings') = 'sgniteerG'<br>



~~~
function reverse(str) {
	let reversed = '';

	for (let character of str) {
		reversed = character + reversed;
	}
	return reversed
}

~~~
___

We create a function called reversed with an argument named *str* , then we initiliaze a variable called reversed into a empty string so it will be populated later.
<br>
We create for of loop to loop the individual letters. For further and better explanation we will use the example "apple".
With the for of loop we loop the individual letters one by one. Then we use the previously created variable reversed ( remember we initialized to empty string so can be populated ). And inside the loop we write this statemenet reversed = character + reversed.
<br>
First character as you can see is variable that we choose to represent the individiual letters. Now let's imagine => 
'' = character(letter) + '' => the result will be '' = a + '' which will be concatenated to  '' = a Second iteration will be a = p + a  => a = pa
Third iteraration will be  pa = p + pa => a = ppa
Fourth iteration will be ppa = l + ppa => ppa = lppa
Fifth iteration will be  lppa = e + lppa => lppa = elppa
If there are no more letters from the loop we return reversed.
And in our case reversed = elppa
