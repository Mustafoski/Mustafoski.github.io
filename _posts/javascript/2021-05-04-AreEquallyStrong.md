---
layout: post
title: "AreEquallyStrong"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2021-05-05T15:39:55-04:00
modified: 2021-05-05T15:39:55-04:00
---


## AreEquallyStrong 
Call two arms equally strong if the heaviest weights they each are able to lift are equal.

Call two people equally strong if their strongest arms are equally strong (the strongest arm can be both the right and the left), and so are their weakest arms.

Given your and your friend’s arms’ lifting capabilities find out if you two are equally strong.
___

> ##For Example
console.log(AreEquallyStrong(10,15,15,10)) true
console.log(AreEquallyStrong(15,10,15,10)) true
console.log(AreEquallyStrong(15,10,15,9))  false

##
<br>


~~~
function AreEquallyStrong(yourLeft,yourRight,friendsLeft,friendsRight){
  const yourWeakest = yourLeft <= yourRight ? yourLeft : yourRight;
  const yourStrongest = yourLeft >= yourRight ? yourLeft : yourRight;
  const friendsWeakest = friendsLeft <= friendsRight ? friendsLeft : friendsRight
  const friendsStrongest = friendsLeft >= friendsRight ? friendsLeft : friendsRight

  return (yourStrongest === friendsStrongest && yourWeakest === friendsWeakest);


}

console.log(AreEquallyStrong(10,15,15,10))
console.log(AreEquallyStrong(15,10,15,10))
console.log(AreEquallyStrong(15,10,15,9))
~~~

