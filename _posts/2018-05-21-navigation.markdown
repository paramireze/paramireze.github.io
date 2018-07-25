---
layout: post
title: "Adding View and Navigation Controller"
date: 2018-05-21 07:30:00 -0500
categories: iOS Development 
---

XCode makes it easy to add additional views to your application using drag and drop functionity. I am able to create a visual representation of my application without writing code. This has the advantage of having a proof of concept application without using wireframes, diagramming or other deplorable practices.

![Navigation Controller]({{ "/assets/images/2018/may/navigation_controller.png "}}) 

The starting point of every iOS app is the root view controller. That is the screen that displays when you first open the application. I created a `Navigation Controller` that will embed into the `Root View Ctonroller`. the Navigation Controller makes it so the application can link together additional views that are stacked on top of the `Root View Controller`.  
