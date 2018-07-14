---
layout: post
title: "Setting up Navigation"
date: 2018-07-14 09:00:00 -0500
categories: iOS Development 
---

adding navigation is done through the `navigation stack` using `navigation controllers`. We use `Segues` to communicate between each `navigation controller`. 

# Adding `Navigation Controller` the XCode way
The `Navigation Controller` becomes a container for the `Root View Controller` aka the `Meal Table View Controller`. 

![adding navigation]({{ '/assets/ios/july/adding_nav.png' }})


## Custumizing the Nav Bar
Once we implement the `Navigation Controller`, a top portion of each view controller will be reserved for navigation controls. We are able to set the navigation title property for each view controller so each scene has a unique title. I think add a `+` link so users are able to navigate to the create meal controller

![navigation title and add link]({{ '/assets/ios/july/nav_title_and_add_link.png' }})

## Final Result
Hey we did it!

![We Did it!]({{ '/assets/ios/july/app_with_nav_bar.png' }})

