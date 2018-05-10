---
layout: post
title: "iOS UI design in XCode"
date: 2018-05-10 07:20:50 -0500
categories: iOS Development 
---
Today we attached an event handler to the button click action. I was able to do this using XCodes control-click functionality and dragging an arrow to the `ViewController`. By doing that, we are able to create methods that are accessible to the `Interface Builder` which will handle the UI actions for us.

![workflow diagram]({{ "/assets/ios/may/update_label.png" }})

## Concepts groked since last post

### Singleton
defining a class as a singleton will ensure that only one object is instantiated. This can be useful for making global variables which would should never be duplicated in any circumstance. 

### AppDelegate getswifty file (couldn't resist)
 
The `AppDelegate.swift` file is used to detect changes in state. You are able to use the methods to perform tasks when an app is finished launching or about to terminate

