---
layout: post
title: "The First Responder"
date: 2018-06-14 08:00:00 -0500
categories: iOS Development 
---

An application is able to create an interface through the use of the `UIKit framework`. Everytime a new element is added to the GUI, a `UIView` object is created and all mapped in a hierarchal structure using super/sub view relationships. For example, when a developer adds a text field to the `UIView`, a `UITextField` object is created which is a sub view in the hierarchy.  

![UI Kit Framework]({{ '/assets/ios/june/ui_kit.png' }})

Understanding how the view hierarchy works can be useful when trying to understand how event handling is done in iOS. Basically, all event driven interactions are done through `Responder` objects. A responder object is any instance of the `UIResponder` class which includes the subclasses `UIView, UIViewController, and `UIApplication`.

A good use case might be, a user selects a text field. `UIResponder` class directs the event to the most appropriate `responder` object. The `Responder` object then can handle the user input/actions with pre-defined logic specific for that UI element.

![View Hierarchy]({{ '/assets/ios/june/view_hierarchy.png' }})

Personal note: This is my best stab at responder objects and believe their are many gaps in my understanding. 
