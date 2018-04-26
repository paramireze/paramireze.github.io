---
layout: post
title: "Ruby Rails Asset Pipeline"
date: 2018-04-26 10:40:50 -0500
categories: Ruby Rails development
---

I never really took the time to learn asset pipelines. I always had used the default configuration to work with bootstrap and never gave it a second thought. I am now in a situation where I need to use custom styles. 

the `asset pipeline` provides a framework to concatenate and minify or compress JavaScript and CSS assets. In short, it is a way to manage assets used among various gems in a simple way.

`concating assets` - is a way of reducing number of requests a browser makes to render a webpage.

`sprockets` - library for compiling and serving web assets. Allows for multilanguaging managment such as coffeescript, sass and scss. `Sprockets` will concatenate all javascript files into one master.js and all css into a master.css file

`fingerprinting` - technique used to `bust cache` by changing the filename anytime a file is updated. This would havebeen especially useful to me when working in codeigniter and I had to keep changing the filename manually by concating an integer at the end of the filename.

