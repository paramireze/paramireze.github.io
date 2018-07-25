---
layout: post
title: "Fun with Stackviews"
date: 2018-05-15 07:30:00 -0500
categories: iOS Development 
---

In one of the tutorials, I noticed I was having a difficult time understanding how to get the UI elements to line up right. So I do what I normally do when I get stuck and frustrated, I read. In an article by `Medium`, they had a small tutorial working with `stackviews`. Basically, the goal was to line up your column and rows of elements inside stackviews. Once the elements and stackviews were created, we then created constraints for the stackviews fr the `alignment`, `spacing`, and `distribution` properties. Once those were set, then the spacing of the form elements were distributed equally within their stackviews and displayed nicely among the various screen sizes and portrait/landscape mode.

![Stackview demo screenshot]({{ "/assets/images/2018/may/stack_view.png" }})

From what I have read with my limited knowledge, stackviews is an alternative to `autolayout`. `Autolayouts` will dynamically calculate the gui elements for you. However, the problem is you have to then set constraints for each of those elements. It can then become difficult to move elements around or make changes since those constraints would then be broke by changes. Also, I read that autolayout adds a lot of complexity to an applications interface. Just something to be aware of... autolayout baaaddd, stackview goooood.... me smash!
