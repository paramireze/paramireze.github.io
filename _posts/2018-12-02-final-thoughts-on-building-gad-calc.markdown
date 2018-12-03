---
layout: post
title: "My First iOS App: Gadolinium Calculator v2"
date: 2018-09-14 12:00:00 -0500
categories: iOS Development
---

After several months of tutorials and building demo iOS apps, I finally got around to building the real thing.
My brother built the original Gadolinium Calculator app using C# about two years ago.
A request was put in to have a second version of the app to make the table view sortable/deletable.
I thought it fitting that I would build the second version.

![Table View]({{ '/assets/images/2018/dec/gadCalc1.png' }})

It was thought that building the app from scratch using swift would be easier than using the original code that was done in c#.
The reason being is swift provides build in sorting/deleting functionality for table views.

## A different mindset
Mobile development forced me to be more of a designer than a back end developer.
Every element on a given view required a lot of time and consideration.
I like how I could connect each page element to the view controller so I had full control over the user experience.
  
![Calculator]({{ '/assets/images/2018/dec/gadCalc3.png' }})

## Stackviews
Building the layout was greatly simplified using stackviews. 
One tutorial said to use them often, since they can provide consistent layout across all devices.

![Storyboards]({{ '/assets/images/2018/dec/gadCalc2.png' }})

## Strong Type Programming Language
I do a lot of programming using ruby and php which are both loosely typed languages.
Swift is freaking awesome at ensuring things are exactly what they are supposed to be.
I can see now why people may not like scripting/weak type languages such as php. 
However, I am not one of those people.
I believe good programming conventions can make code highly dependable regardless of the language.
Albeit, I might be more hesitant to approach code written in a weak typed language if I think it was developed by someone who is not familiar with best practices.




