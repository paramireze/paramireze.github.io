---
layout: post
title: "Cancel And Delete Functionality"
date: 2018-07-24 10:00:00 -0500
categories: iOS Development
---

I will be persisting the Meal class data using the `NSCoding` protocol. I subclass the `NSObject` to override the `encordeWith` methods.

# step 1: implement encodeWithCoder method
the `encodeWithCoder` allows for class information to be archived. 
This is where you set 