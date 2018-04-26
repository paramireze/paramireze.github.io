---
layout: post
title: "Time to implement a Loader into weather app"
date: 2018-04-24 18:45:40 -0500
categories: More Loader Stuff
---
In the latest exercise, we want to offload most of the logic into loaders. This will free up the main ui thread, allowing for better resource management. This means much faster load times when the app state changes after being destroyed.

lets get some things out of the way. Our fancy pants app passes in a `callback` to the `initLoader` class within the `LoadManager.java`. My initial understanding from the documentation is that the `initLoader` is called everytime a state is changed. From what I can tell, the main purpose of this class is to execute the `onLoadFinished()` once the loader has a) been started b) data is loaded. This allows for 
 
# Old Behavior
The old behavior was for the weather app to look up the json data in the main thread.

# New Behavior
we are using loaders to break up the tasks using the three loader functions

1. `onStartLoading()`
2. `loadInBackground()`
3. `deliverResults()`


1. when using AsyncTaskLoader, within the closure, you must implement the `AsyncTaskLoader` subclass `onStartLoading`. `onStartLoading` will load any cached data to avoid duplicating processing.

2. 
