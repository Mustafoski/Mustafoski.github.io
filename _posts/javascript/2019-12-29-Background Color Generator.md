---
layout: post
title: "Background Color Generator"
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

## Background Color Generator




~~~
document.querySelector('button').addEventListener('click', function () {
    document.body.style.backgroundColor = runColor();
})

function runColor() {
    return '#' + Math.random().toString(16).substr(-6)
}
~~~
___

1. In the index.html we have button where we listen for an event click then we style the whole body with document.body.style.backgroundColor = runColor();

2. runColor() is a helper function that returns random decimals then we use string method to convert them to strings in hexadecimal format and we use another string method substr(-6) to take out 6 numbers also in the front we add '#' to be hexadecimal format of color