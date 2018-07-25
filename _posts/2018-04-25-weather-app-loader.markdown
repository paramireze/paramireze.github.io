---
layout: post
title: "Time to implement a Loader into weather app"
date: 2018-04-24 18:45:40 -0500
categories: More Loader Stuff
---
[sunshine exercise 5.01]({{ "https://classroom.udacity.com/courses/ud851/lessons/ed13cc93-2861-43bf-b7ed-395a166ab975/concepts/f0467b0c-62d7-4551-8ece-c56769f46643" }})

In this exercise we are moving from `AsyncTask` to `AsyncTaskLoader`. `AsyncTask` is not good for resource management when it comes to changing activity states. For example, if the user rotates their screen, then the app is recreated from scratch and all data has to be reloaded. `AsyncTaskLoader` will cache the state of the activity so in the event of a state change, the data is readily available.


lets get some things out of the way. Our fancy pants app passes in a `callback` to the `initLoader` class within the `LoadManager.java`. My initial understanding from the documentation is that the `initLoader` is called everytime a state is changed. From what I can tell, the main purpose of this class is to execute the `onLoadFinished()` once the loader has a) been started b) data is loaded. This allows for 
 
To best understand the workflow of loadmanagers, i found a useful diagram

![load manager image]({{ "/assets/images/2018/jan-june/LoaderManager_Loader.png" }})

# Old Behavior
Use the `loadWeatherData()` in the main thread. 

# New Behavior
we are using loaders to break up the tasks using the three loader functions

1. `onStartLoading()`
2. `loadInBackground()`
3. `deliverResults()`


1. when using AsyncTaskLoader, within the closure, you must implement the `AsyncTaskLoader` subclass `onStartLoading`. `onStartLoading` will load any cached data to avoid duplicating processing.

2. 
