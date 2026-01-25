---
layout: post
title: "Monotonic Array Check"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2024-03-12T15:39:55-04:00
modified: 2024-03-12T15:39:55-04:00
---

# Monotonic Array Check

## Definition
An array is **monotonic** if it is either:
- **Non-decreasing** (each element is greater than or equal to the previous one), or
- **Non-increasing** (each element is less than or equal to the previous one).

Single-element arrays are always monotonic.

---

## Function Purpose
The `checkMonotonic` function checks whether a given array follows a monotonic order.

---

~~~
const checkMonotonic = function (array){
    const first = array[0];
    const last = array[array.length-1];
// 1.......10
    if(first === last){
        for(let i=0;i<array.length-1;i++){
            if(array[i+1]!==array[i]) return false;
        }
    }
    else if (first<last){
        // non decreasing
        for(let i=0;i<array.length-1;i++){
            if(array[i+1]<array[i]) return false;
        }
    }
    else{
        // non increasing
        for(let i=0;i<array.length-1;i++){
            if(array[i+1]>array[i]) return false;
        } 
    }
    return true;
}

checkMonotonic([9]);
~~~





## How It Works

1. **Identify Direction**
   - Compare the first and last elements of the array.
   - This determines whether the array should be:
     - Constant
     - Increasing (non-decreasing)
     - Decreasing (non-increasing)

2. **Validate Order**
   - Traverse the array once.
   - At each step, compare the current element with the next one.
   - If the expected order is violated, return `false`.

3. **Return Result**
   - If no violations are found, return `true`.

---
