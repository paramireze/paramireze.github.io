---
layout: post
title: "Customizing Custom Controls"
date: 2018-07-07 09:00:00 -0500
categories: iOS Development 
---

Dynamically generating buttons in the mobile app is a much different experience than typical form creation. Normally, i would use html elements and attributes to add buttons, and then add javascript to do any event handling or maybe make a form submit/link control. 

The thing I like about swifts/xcodes way of creating custom controls is the separation of logic. I am able to tightly control the customizations for a specific area of the mobile app and keep everything nicely organized in a file. In this case, I am able to dynamically create the buttons, assign properties, and add event handler method that will asyncronously update the form behind the scenes. 

![star images]({{ '/assets/ios/july/starImages.png' }})
