---
layout: post
title: "An argument against Storyboards"
date: 2018-07-03 20:00:00 -0500
categories: iOS Development 
---

In this post, I am summarizing an article by `Medium.com`. https://medium.com/ios-os-x-development/interface-builder-is-great-storyboards-are-not-69232a91044e

# Storyboards are not for everyone
Storyboards have a few problems that make it less than ideal to work with. It is often the case that storyboards will have git merge conflicts when a team is working on the same project. The reason being is that storyboards often share logic throughout an application. 

# Crashability
An application is more likely to crash when using storyboards because of its use of `mutable variables`. Basically, a storyboard can have a dependancy on another storyboard such as a variable being passed by a `segue`. If that data is incorrect, then the system crashes.

# Less Modular
Storyboards with `segues` will have cause a dependency. That means careful consideration will need to take place before changes are made to one storyboard. 

I personally think I would like storyboards more, despite the disadvantages listed. I like the visual aspect. I like making diagrams of things to explain workflows. Furthermore, I like to think that I am someone who is willing to put in the extra work to have a more desirable outcome.
