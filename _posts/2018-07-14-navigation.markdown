---
layout: post
title: "Navigation and Segways and Segues"
date: 2018-07-14 09:00:00 -0500
categories: iOS Development 
---

![Segue]({{ '/assets/ios/july/segue.jpeg' }})

When I first heard about `Segue's` in iOS, I immediately thought of `segways` and thought they decided to spell it differently.
My brother also thought it was weird the spelling difference and I eventually google searched the word.
`Segue` is "to transition" and `segway` is a name of the product.
Thanks Bryan for making me aware of the unusualness of the spelling that lead up to my search.
I am working with iOS segue's for navigating between controllers and pass data when needed.

## The Navigation Stack
I will be implementing a `Navigation Controller` to manage navigtion between the `Food Review List` view controller and the `Food Review Details` view controller.
A `navigation controller` provides the toolbar at the top of each scene and can be used to add navigation buttons.
Navigation controllers use what is called the `navigation stack` which adds or removes view controllers from an array.

## Modal Segues vs Push Segue
At its most basic level, a `Modal Segue` is anytime you want to send the user to another screen and have them come back again with update or new data.
For example, clicking the  `Add Item` button will open up a modal page where a user can enter or edit a review.
When done, the user is sent back to the list page and the new review will display.
A `Push Modal` is adding another view controller to the navigation stack.

![View Controllers]({{ '/assets/ios/july/nav_diagram.png' }})

# Adding `Navigation Controller` the XCode way
The `Navigation Controller` becomes a container for the `Root View Controller` aka the `Meal Table View Controller`. 

![adding navigation]({{ '/assets/ios/july/adding_nav.png' }})

## Custumizing the Nav Bar
I added a title and a `+` link so users are able to navigate to the create meal controller.

![navigation title and add link]({{ '/assets/ios/july/nav_title_and_add_link.png' }})


![Add the Segue]({{ '/assets/ios/july/IN_addbutton_drag_2x.png' }})

## Unwind Segue
the `Unwind` segue method is provided to return the users controller in the event the back button is hit.

## Final Result
added some form validation and other basic functionality and Walla! questo è fantastico!

![We Did it!]({{ '/assets/ios/july/app_with_nav_bar.png' }})

