---
layout: post
title: "Navigation and Segways and Segues"
date: 2018-07-14 09:00:00 -0500
categories: iOS Development 
---

![Segue]({{ '/assets/ios/july/segue.jpeg' }})

TIL `segue` is to transition and `segway` is a product. Anyways, I am now at the point that I have two fully operational `View Controllers`. The next step to build the Meal Tracker app is to add a `Navigation Controller`. Navigation controllers provides the navigation controls for each scene. It will also manage a `View Controller` hierarchy.

# View Controllers
a `View Controller` is a view that handle navigation controls for a page. View controllers are organized in the Navigation Controllers `Navigation Stack`. The  navigation stack is how the various scenes are organized when someone uses the navigation controls. Developers can then use `segues` to manage adding or removing view controllers from the stack. 


![View Controllers]({{ '/assets/ios/july/nav_diagram.png' }})

# Adding `Navigation Controller` the XCode way
The `Navigation Controller` becomes a container for the `Root View Controller` aka the `Meal Table View Controller`. 

![adding navigation]({{ '/assets/ios/july/adding_nav.png' }})


## Custumizing the Nav Bar
Once we implement the `Navigation Controller`, a top portion of each view controller will be reserved for navigation controls. We are able to set the navigation title property for each view controller so each scene has a unique title. I think add a `+` link so users are able to navigate to the create meal controller

![navigation title and add link]({{ '/assets/ios/july/nav_title_and_add_link.png' }})


## Push Segue vs Modal Segue
so easy to do.

![Add the Segue]({{ '/assets/ios/july/IN_addbutton_drag_2x.png' }})

## Unwind a Segue
I will be a `unwind segue` to return the meal object after the user has either saved or cancelled a new meal review. Segues use the `prepare(for:sender:)` method for custom logic to be executed before the segue is executed 

## Final Result
Hey we did it!

![We Did it!]({{ '/assets/ios/july/app_with_nav_bar.png' }})

