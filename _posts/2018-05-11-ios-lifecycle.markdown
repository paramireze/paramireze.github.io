---
layout: post
title: "View Controller Life Cycle"
date: 2018-05-11 20:20:50 -0500
categories: iOS Development 
---

The `UIViewController` class has several methods. Each method is meant to solve a different problem. In this case, it is executing code at different states of the iOS application.

1. `viewDidLoad`
2. `viewWillAppear`
3. `viewDidAppear`
4. `viewWillDisappear`
5. `viewDidUnload`

I have a basic understanding of the listed methods. I read that `viewDidLoad` is useful for one time operations. `vieWillAppear` is good for handling html manipulation before the screenloads. `viewDidAppear` is good for running longer operations and presenting a spinwheel for loading. 


These methods are not accessible through the `UIView`, only the `UIViewController`. 

## viewDidLoad vs viewWillAppear

`viewDidLoad` is when the view is first loaded into cache. It is not yet displayed. `viewWillAppear` method is executed just  before the view is displayed, making it ideal for hidding/showing html page elements.

