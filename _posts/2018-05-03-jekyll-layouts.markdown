---
layout: post
title: "Creating Layouts by Overriding the Defaults"
date: 2018-05-03 16:44:00 -0600
categories: "Jeykll"
---

#Good morning
It has been fun learning exactly  what `Jekyll` is. Jeykll is a blogging framework that allows people to build  content management system (CMS) using folders and files. This is a different approach to building a CMS than wordpress because wordpress's uses a database.

Not having to deal with a database offers some cool benefits. However, for the sake of sticking to theme of this particular post, I will discuss that more in another post. Besides, I am still learning the framework and will be able to give a better analysis later on.

# Changing the home page
Today, I changed the layout of the home page. I show an excerpt and category title so it is more clear what my content is about without having to click in.

# Home Page Before
![Before]({{ "/assets/jekyll/layout_before_category.png" }})

# Home Page After
![After]({{ "/assets/jekyll/layout_add_category.png" }})

I was able to do this by overriding the default layout page `home.html`. This file is located outside of my project in a theme folder. I had to create a copy of the theme's `home.html` file and paste it into a location inside my project following `jekylls` directory structure convention. In this case, I had to create a `_layout` folder at the root level and place `home.html` inside of it. 

Jekyll is able to detect my local version of `home.html` using `Liquid templating language`. Basically, `Liquid` allows users to override the default theme layout by creating a local version in their project. The framework knows to check your project first and then the original theme after.

