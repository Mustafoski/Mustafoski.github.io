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

Translator

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
We load all the languages in a array called langs in the HTML we have to inputs From a language To a language and we take them as IDs and in the text area we translate the inserted words. first we take the API, then we check if the API has response.status of 200 (success) if not return Errror.

If response.status is 200 we use json() on the response and create callback where take the written sentence and translate it or if error last line will cought the errror with catch.
