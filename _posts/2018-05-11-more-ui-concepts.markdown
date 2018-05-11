---
layout: post
title: "Constraint Layout continued"
date: 2018-05-11 07:20:50 -0500
categories: iOS Development 
---
I was able to position the UI elements on the page using constraints. I made sure they display as I want them for all devices. I achieved this goal by setting up constraints for each of the layouts. I linked each element to one another as opposed to the position relative to the screen. It is important to do it this way since the user can switch from landscape to potrait.


So far, all our buttons and labels have been done using Apple's `UI Kit`. UI kit provides preconfigured UI elements to allow developers to create a UI quickly.

While working with `Interface Builder` you are able to see filled in circles in the XCode IDE, next to the line number, which indicates that an action is mapped to a UI element.

`IBOutlet` is the code that interacts with the UI
`IBInput` logic that executes after triggering an event

My favorite quote from this exercise

> In programming, you have to keep the attitude of a child. You have to be willing to experiment and to try new things. 
