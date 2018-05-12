---
layout: post
title: "View Controller Life Cycle"
date: 2018-05-11 20:20:50 -0500
categories: iOS Development 
---

the `UIViewController` lifecycle can be broken up into four parts; `appearing`, `appeared`, `disappearing`, `disappeared`. An app dev can then use methods that are executing, before and after each event. Each of these four parts can be considered stages. And these stages are important to understand when it comes to executing code since it will have an impact on performance, appearance and load times. 

