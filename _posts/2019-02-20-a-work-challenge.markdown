---
layout: post
title: "A Seemingly Simple Problem"
date: 2019-02-19 07:00:00 -0500
categories: Work
---

Each year, faculty at the University have to enter in data for their `published peer-reviewed manuscripts`. 
 Basically, they copy and paste data from a spreadsheet into form fields in a application.
 I am being asked to add functionality to the application which would allow the faculty to copy all of the excel data and paste it into the application to save time. 

## the application 

 The application in question is a financial tool, used to track faculty activity.
 It is a CMS app built in Code-Igniter/PHP.
 All data, form fields, inputs, etc is data driven.

## my role
 The application was handed off to radiology in 2013 and I have sinced been the primary person to support the application. 

## todo 

 1) detect `IF published-Peer-Reviewed-Manuscripts`
 2) preserve the excel formatting 
 3) store/retrieve the data from the database

# 1) detecting `IF peer-reviewed manuscripts`
 Since everything is data driven, I will need to check which question is being asked. 
 I will need to query each `question id` against the database to see if it belongs to `published-Peer-Reviewed-Manuscripts`.
 Luckily performance isn't an issue.

# 2) parsing the excel formating
 I will need to write php code that will preserve and display the excel data. 

 here is what a javascript solution looks like.. will need to implement in php

{% highlight ruby %}

    <script type="text/javascript">
       $(function() {
           $('textarea[name=excel_data]').keyup(function() {
               var data = $(this).val();
               var rows = data.split("\n");
               var table = $('<table />');    
               for(var y in rows) {
                   var cells = rows[y].split("\t");
                   var row = $('<tr />');
                   for(var x in cells) {
                       row.append('<td>'+cells[x]+'</td>');
                   }
                   table.append(row);
               }
               $('#excel_table').html(table);
           });
       });
    </script>

{% endhighlight %}
    
# 3) store/retrieve the data from the database
 Since everything is database driven, i will need to refactor the `published peer-reviewed manuscripts` category and configure it to have a text area question instead of the many form fields.
 
 this means that the php code needs to know to check for excel delimiters such as `\t`, `\n`, `<table>`, `<tr>`, `<td>` and 
     
# storing the data
 I do not see this being too big of an issue. I will need to make sure that none of the formatting is stripped in the table data field.
  
# additional considerations 
 What happens if someone updates the form builder plugin? Well, my custom logic will get overridden and it will seize to work for storing excel data.
 This problem can be avoided if time were invested in implementing an overridable method that allows for custom logic without touching the plugin source code.
 However, that is not a luxery I am being given, especially with other deadlines looming. 
 What is worse, this type of lack of upfront investment will ultimately cost much more later when things break and no one knows why or how to fix it. 
 Such is life of a developer working in a large organizations where such things are next to impossible to communicate.    






