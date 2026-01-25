---
layout: post
title: "Are Equally Strong"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2022-03-13T15:39:55-04:00
modified: 2022-03-13T15:39:55-04:00
---

Are Equally Strong
<br><br>
Call two arms equally strong if the heaviest weights they each are able to lift are equal.
Call two people equally strong if their strongest arms are equally strong (the strongest arm can be both the right and the left), and so are their weakest arms.
Given your and your friend's arms' lifting capabilities find out if you two are equally strong.

**Example**<br>
console.log(areEquallyStrong(10, 15, 15, 10)) true<br>
console.log(areEquallyStrong(15, 10, 15, 10)) true<br>
console.log(areEquallyStrong(15, 10, 15, 9)) false<br>




~~~
function areEquallyStrong(yourLeft, yourRight, friendsLeft, friendsRight) {
  const yourWeakest = yourLeft <= yourRight ? yourLeft : yourRight;
  const yourStrongest = yourLeft >= yourRight ? yourLeft : yourRight;
  const friendsWeakest = yourLeft <= yourRight ? yourLeft : yourRight;
  const friendsStrongest = yourLeft >= yourRight ? yourLeft : yourRight;


  return (yourStrongest === friendsStrongest && yourWeakest === friendsWeakest);
}

console.log(areEquallyStrong(10, 15, 15, 10)) true
console.log(areEquallyStrong(15, 10, 15, 10)) true
console.log(areEquallyStrong(15, 10, 15, 9)) false

~~~



We create function called areEquallyStrong with parameters *yourLeft*, *yourRight*, *friendsLeft*,   *friendsRight*
<br><br>
We create four (4) variables <br>
1. **yourWeakest** = *yourLeft <= yourRight ? yourLeft : yourRight*
<br><br>
2. **yourStrongest** = *yourLeft >= yourRight ? yourLeft : yourRight*;
<br><br>
3. **friendsWeakest** = *yourLeft <= yourRight ? yourLeft : yourRight*;
<br><br>
4. **friendsStrongest** = *yourLeft >= yourRight ? yourLeft : yourRight*;
<br><br>
In the end we **return (*yourStrongest* === *friendsStrongest* && *yourWeakest* === *friendsWeakest*)