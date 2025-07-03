---
layout: post
title: "Sorting Array of Objects and Arrays"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2023-02-11T15:39:55-04:00
modified: 2023-02-11T15:39:55-04:00
---

Sorting Array of Objects and Arrays
<br><br>

Sorting an array of objects or arrays means arranging the elements of the array in a particular order based on some criteria. This can be done in ascending or descending order based on a specific attribute or property of the objects or arrays, such as alphabetical order, numerical order, or date order. The sorted array will have the elements rearranged in a way that satisfies the sorting criteria.
<br>
**Example**<br>
let people = [{<br>
    firstname:'Bob',<br>
    lastname:'Zimmerman',<br>
    age:47<br>
},{<br>
    firstname:'Bob',<br>
    lastname:'Smith',<br>
    age:45
},{<br>
    firstname:'Bob',<br>
    lastname:'Smith',<br>
    age:23<br>
},{<br>
    firstname:'Sue',<br>
    lastname:'Lee',<br>
    age:33<br>
}];<br>
<br><br>

[[object Object] {
  age: 23,
  firstname: "Bob",
  lastname: "Smith"
}, [object Object] {
  age: 33,
  firstname: "Sue",
  lastname: "Lee"
}, [object Object] {
  age: 45,
  firstname: "Bob",
  lastname: "Smith"
}, [object Object] {
  age: 47,
  firstname: "Bob",
  lastname: "Zimmerman"
}]




~~~
let people = [{
    firstname:'Bob',
    lastname:'Zimmerman',
    age:47
},{
    firstname:'Bob',
    lastname:'Smith',
    age:45
},{
    firstname:'Bob',
    lastname:'Smith',
    age:23
},{
    firstname:'Sue',
    lastname:'Lee',
    age:33
}];

people.sort(function (a, b) {
    let ageComparison = a.age - b.age;


    if (ageComparison === 0) {
        let lastNameComparison = a.lastName.localeCompare(b.lastName)
    
        if (lastNameComparison === 0) {
                ***return a.firstname.localeCompare(b.firstname);***
        }
        return lastNameComparison;
    }
    return ageComparison;
    });
    console.log(people)
~~~


This code sorts an array of objects "people" based on the "age" property of each object. The sort function takes in a callback function that compares two objects "a" and "b" by subtracting the age of "b" from the age of "a". This results in a negative value if "a" is older than "b", a positive value if "a" is younger than "b", and zero if they have the same age.<br><br>

If the age comparison results in a tie, the function then compares the "lastName" property of each object using the "localeCompare" method, which returns a value indicating the alphabetical order of the strings. If the last names are the same, the function then compares the "firstName" property of each object using "localeCompare" again.<br><br>

The sort function then returns the comparison result, which is either the age comparison, the last name comparison, or the first name comparison, depending on the tiebreaker. This sorting algorithm thus sorts the "people" array first by age, then by last name, and finally by first name.<br><br>

The result of the sort operation is then printed to the console using the "console.log" function, which outputs the sorted "people" array.<br><br>