---
layout: post
title: "Gesture Recognizer"
date: 2018-06-20 08:00:00 -0500
categories: iOS Development 
---

In this post I would like to answer the question "What is the difference between a `control`, a `delegate`, and a `gesture recognizer`. The three are major compontents to user interaction with the `UIKit Framework` and it is not clear to me their responsibilities.

# Control
A control is an object assigned to a view that will interact with the user. For example, when a user taps into a text field, a control object will signal that the phone's keyboard should pop. 

# Delegate 
The only way I can comprehend delegates is thinking of them as event handlers. You define event handlers aheado of time to execute certain code when certain events take place. Delegates are a bit more robust than a simple `JS` event handler in that it has protocols in place that detect various types of events with default method calls on each event. 

![control diagram]({{ '/assets/images/ios/june/control_diagram.jpg' }})

# Gesture Recognizer
From my very limited knowledge of gesture recognizers, I believe they are a way to customize UI Elements to mimick behaviors of controls. `Gesture Recognizers` allow a UI Element (Image, label, etc) to detect certain gestures (tap, swipe, pinch, etc) to trigger an event such as showing a keyboard. 

In conclusion, I think controls are predefined objects with their own set of methods used to quickly get a interface working for a user. Gesture recognizer's are objects that can create controls for UI elements and delegates are the objects that will communicate with the `control` and `gesture` objects to handle triggered events.
