---
layout: post
title: "Page Layouts using Embedded Ruby (ERB)"
date: 2018-05-11 13:15:00 -0500
categories: Ruby Rails development
---

I have a bad habit of memorizing syntax for a given language and never really understanding what is going on. Frameworks make it easy to ignore all the things going on in the background and I want to get out of the habit of never really understanding what is happening. 

Ruby rails uses a templating system called `eRuby` also known as `embedded ruby` or `ERB`. When a file has an `erb` extension, ruby knows to evaluate all code within a ruby tag. There are two types of tags that lets ruby know to evaluate content. First is the `<%` tag which will run the code as a scriplet. The other is `<%=` which is known as an expression and outputs the content as html. 

### Ruby Version
the current version of Ruby is 2.5.1

### Ruby Interpreter 
The original interpreter for Ruby is `Matz` (aka MRI), named after `Yukihiro Matsumoto`, the ruby creator. `Matz` last stable version is back in 1.8.7 in 2013.

[Yukihiro Matsumoto]({{ "/assets/images/rails/may/matsumoto.jpg" }})

### The ruby name
it came from an online chat exchange between Matsumoto and Keiju Ishitsuka in 93. Matsumoto chose Ruby because it is the birthstone of one of his collegues. 


For the project I am working on, I had to read up on documentation for best practices when it comes to creating a link using ruby rails. The `link_to` is a method found in the `URL Helper`. According to the ruby documenation 'It provides a set of methods for making links and getting URL's that depend on the routing subsystem'. 

