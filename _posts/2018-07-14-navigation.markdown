---
layout: post
title: "Navigation and Segways and Segues"
date: 2018-07-14 09:00:00 -0500
categories: iOS Development 
---

![Segue]({{ '/assets/ios/july/segue.jpeg' }})

TIL that `segue` is "to transition" and `segway` is a name of the product. Anyways, I am now at the point where I have two fully operational `View Controllers`. 
My next step will be to implement navigation using the `Navigation Controller`. 
Navigation controller provides the controls at the top of each scene .

## The Navigation Stack
Navigation controllers are used to manage view controllers in what is called a `Navigation Stack`. The navigation stack is essentially an array of view controllers that were added to the stack. When the user hits the back button, the view controller is removed from that array.

## Modal Segues vs Push Segue
If a user taps a meal from the table view, the app will open a details page that allows the user to update information. To make that happen, we would have to pass the selected `Meal` information to the details page. For that reason, I will need to use a `Modal Segue` to open that view controller. Using a `Modal Segue` navigation will create a parent & child view controller relationship since the `details page` will always be closely tied to a selected item from the parent page.

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

