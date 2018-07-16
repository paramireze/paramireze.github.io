---
layout: post
title: "Navigation and Segways and Segues"
date: 2018-07-14 09:00:00 -0500
categories: iOS Development 
---

![Segue]({{ '/assets/ios/july/segues.jpeg' }})

This is my second iOS tutorial and now an expert ;). The general workflow seems to be create two view controllers. Get them fully operational far as UI layout and buttons clicks. Set up a data model and initialize data. Then you add Navigation. This makes a lot of sense and is a good workflow in general far as MVC style goes. 

# Adding `Navigation Controller` the XCode way
The `Navigation Controller` becomes a container for the `Root View Controller` aka the `Meal Table View Controller`. 

![adding navigation]({{ '/assets/ios/july/adding_nav.png' }})


## Custumizing the Nav Bar
Once we implement the `Navigation Controller`, a top portion of each view controller will be reserved for navigation controls. We are able to set the navigation title property for each view controller so each scene has a unique title. I think add a `+` link so users are able to navigate to the create meal controller

![navigation title and add link]({{ '/assets/ios/july/nav_title_and_add_link.png' }})


## Add the Segue
so easy to do.

![Add the Segue]({{ '/assets/ios/july/IN_addbutton_drag_2x.png' }})

## Unwind a Segue
I will be a `unwind segue` to return the meal object after the user has either saved or cancelled a new meal review. Segues use the `prepare(for:sender:)` method for custom logic to be executed before the segue is executed 

## Final Result
Hey we did it!

![We Did it!]({{ '/assets/ios/july/app_with_nav_bar.png' }})

