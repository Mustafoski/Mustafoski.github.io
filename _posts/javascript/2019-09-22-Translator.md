---
layout: post
title: "Translator"
comments: true
share: true
modified:
categories: javascript
excerpt:
tags: []
image:
  feature:
date: 2019-09-22T15:39:55-04:00
modified: 2019-09-22T15:39:55-04:00
---

## Translator

<br>
<br>
<!DOCTYPE html>
<html>
<head>
    <title>Translator</title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width ,initial-scale=1">
    <link href="styles.css" rel="stylesheet" type="text/css">
    
</head>

    
    <body onload="loadLanguages();">
    <div class="container">
        <h1> Translator </h1>
        <p>Please enter a word and select languages to from language to what language to be translated the desired input.</p>
        
        
        <div class="inputWrapper">
            <select  id="from" onchange="translatePhrase();"  width=150 style="width:150px" ></select>
            <textarea type="text" cols="40" rows="5"  onchange="translatePhrase();" id="fromPhrase"></textarea>
        </div><!-- InputWrapper -->
        
        <div class="inputWrapper">
            <select  id="to"  onchange="translatePhrase();" width=150 style="width:150px"  ></select>    
            <textarea type="text" cols="40" rows="5" id="toPhrase"></textarea>
        </div><!-- InputWrapper -->
    </div> <!-- end container -->
    <script src="app.js"></script>
    </body>
</html>


    


___
~~~
function loadLanguages(){
    
    const langs = ["eng","pol","fra","deu","es","mk","ara","tr","pt","it"];
    var options = null;
    var from = document.getElementById('from');
    var to   = document.getElementById('to');
    
    langs.forEach(l => {
    options+= '<option>' + l + '</option>';
});
    
    from.innerHTML = options;
    to.innerHTML   = options;
    
}

function translatePhrase(){
    
    
    var from = document.getElementById('from').value;
    var to   = document.getElementById('to').value;
    var phrase = document.getElementById('fromPhrase').value;
    
    var url = "https://glosbe.com/gapi/translate?from=" + from + "&dest=" + to + "&format=json&phrase=" + phrase  + "&pretty=true";
    
    
    fetch(url)
        .then(response => {
        if(response.status !== 200){
            console.error("API failed , Status code: " + response.status);
            return;
        }
        
        response.json().then(data => {
            document.getElementById("toPhrase").value = data.tuc[0].phrase ? data.tuc[0].phrase.text 
            : "" ;
            
        });
        
    }).catch(err => {
        console.error("Fetch error "+ err);
    });
}

~~~
First we use a function inside the body tag called onload="loadLanguages();
<br>
As you can see the project is called translator first we must populate the HTML Hyper Text Markup Language.

We use the div with a class container from beggining to the end of the html tags where inside we will populate the the HTML with elements and I will indroduce you to those elements accordingly.
First we have a  <h1> Translator </h1> h1 is also called header and it goes from h1 to h6 decreasingly.<br>
After that we have paragraph where we give description what to do. e.g. <p>Please enter a word and select languages to from language to what language to be translated the desired input.</p>
this is also how we create paragraph <p> plain text</p><br>

Then we create two Input Wrappers with Select *TO* and *FROM* and inside the both Input Wrappers there are Selectors with id="from" onchange="translatePhrase();" and second one id="to" onchange="translatePhrase();" 
<br>
There are also two inputareas that have *id* of toPhrase and *id* fromPhrase which we will need later when we use javascript.
<br>
JavaScript file we start same as with the html file with function in this case the same function loadLanguages()
<br>
We initialize a constant with various languages provided by "https://glosbe.com" as for the translating every translator has word from a particular language translated to word in particular language.
<br>

var options = null; // we start with eather empty string "" or null since we haven't choose language.
<br>
var from = document.getElementById('from'); 
var to   = document.getElementById('to');
<br>
We get the values From and To so we can loop the langs array with forEach loop and populate the Select and inside Options e.g.
<br>
<SELECT>
    <OPTION></OPTION>
    <OPTION></OPTION>
    ...           ...
</SELECT>
<br>
   langs.forEach(l => {
    options+= '<option>' + l + '</option>';
});
<br>
After populating the html options we choose a language to be From and to be translated To.
    
    from.innerHTML = options;
    to.innerHTML   = options;
<br> 

Now the final phase is to use the translatePhrase function from the HTML Section and program how the translation will be achieved.
<br>
We create a function translatePhrase(){
    
    Then we initialize 3 variables and its values From which language To one Language and the End result or in this case Phrase.
    
    var from = document.getElementById('from').value;
    var to   = document.getElementById('to').value;
    var phrase = document.getElementById('fromPhrase').value;
<br>

We create variable url where we host the Rest API from https://glosbe.com but with additions <br>
https://glosbe.com/gapi/translate?from=" + from + "&dest=" + to + "&format=json&phrase=" + phrase  + "&pretty=true";
<br>
We use our concatinate our from , to and phrase 

    var url = "https://glosbe.com/gapi/translate?from=" + from + "&dest=" + to + "&format=json&phrase=" + phrase  + "&pretty=true";
 <br>   
  We fetch the url , chain an response , then we check if the response.status is different from 200 if so console some error message if not make response to json() and one more chain with then where we use data and fat arrow function we take the value of the phrase and extract it .  
    fetch(url)
        .then(response => {
        if(response.status !== 200){
            console.error("API failed , Status code: " + response.status);
            return;
        }
        
        response.json().then(data => {
            document.getElementById("toPhrase").value = data.tuc[0].phrase ? data.tuc[0].phrase.text 
            : "" ;
            
        });

If this fails we have catch and it throws an Error
        
    }).catch(err => {
        console.error("Fetch error "+ err);
    });
}