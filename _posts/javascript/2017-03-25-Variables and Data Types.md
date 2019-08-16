---
layout: post
title: "Variables and Data Types"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2017-05-25T15:39:55-04:00
modified: 2017-05-25T15:39:55-04:00
---


# Variables and DataTypes

## Setting up

In order to follow the examples throut the course you need a text editor
*	Brackets
*	Visual Studio Code
*	Atom

These are free Brackets it is Adobe’s product and have feature of live preview, Visual Studio Code is very good editor( I recommend it for bigger development ), and Atom is a great GitHub text editor (To be completely honest I haven’t used that much to give recommendation ).


Second you need a browser that is up to date

*	Google Chrome
*	Mozilla Firefox
*	IE

For simplicity sake I will use Mozilla and it’s Scratchpad, for the other parts Brackets and its live version button.

## Variables

What is a variable in JavaScript? 
We can say a variable it is a container for a value (like: Number, Sentence, String, result etc.).
Variables are special containers in memory that contain a value and that their contained values can change.

**For Example:**
~~~
var tony = “I am Ironman !”;
console.log(tony); // I am Ironman !
~~~

Let’s break down this code:

We have a variable (identifiler) and we named it "tony" ; 
We have an assignment operator = ;
And we have the value that contains "tony" in this case "I am Ironman !"

![JavaScript Image1]({{ site.url }}/images/javascript1.jpg)
{: .pull-center}
Note: If you want to use the Scratchpad as in the photo you can do so with Shift+F4 and open developer tool and choose console.
So what happened? 
>1.	We initialize a variable and called *tony* and we set to the value of *I am Ironman !*
>2.	We printed out the value with the help of the native mechanism console.log(tony)
>3.	Then we used the same variable *tony* but now we set it up to *Robert Downey Jr*
>4.	And again we printed the result.

Another special thing about variables is that they can contain just about anything — not just strings and numbers. Variables can also contain complex data and even entire functions to do amazing things. You'll learn more about this as you go along.


Note that we say variables contain values. This is an important distinction to make. Variables aren't the values themselves; they are containers for values. You can think of them being like little cardboard boxes that you can store things in.


One important distinction is that in some programming languages, you declare a variable (container) to hold a specific type of value, such as number or string. Static typing, otherwise known as type enforcement, is typically cited as a benefit for program correctness by preventing unintended value conversions. This is very common in languages like C, C++, C# , Java, Rubi.


JavaScript uses dynamic typing approach meaning variables can hold values of any type without any type enforcement.

Let’s see some example:
~~~ 
var food = 104.44;
var drink = 55.34;
var bill = food + drink;
console.log(bill);
~~~
`
 ![JavaScript Image1]({{ site.url }}/images/javascript2.jpg)
{: .pull-center}

Unlike other programming languages where you need to specify what you are going to use as a container like in our case something that will hold floating number. ( in C  float variable), we just have the container and we care about the value inside the container.

## Naming Convection 
It is best practice to use camel case style of variables like
var addNew
var editHotel
var editHotelRoomNumber
This convection is also practiced in most initializers.
Another naming convection that is largely used is the private initializing starting with _
~~~ 
var _addNew
var _editHotel
var _editHotelRoomNumber
~~~


## Data Types

