---
layout: post
title: "Why Delegates Why"
date: 2018-06-08 16:00:00 -0500
categories: iOS Development 
---

I get the concept of a delegate. You need something from someone and you send a delegate to do the job. Ideally, this person is highly specialized and fit for delegating for a specific purpose. 

What I don't get is how iOS uses delegates. In the documentation, it states that a delegate object is an object that works in cordination with or on behalf of another object. The delegating object keeps a reference to the delegate object and is able to pass information to the object as needed. So, from what I can tell, the reason why you need a delegate is so the UI can change and states while the information is safely tucked away. 

Writing this out makes more sense and I realize that the real issue I am having is understanding what the `self` reference means because in the code you use

`nameTextField.delegate = self`

and it is now obvious to me that `self` is the parent UIViewController object.
