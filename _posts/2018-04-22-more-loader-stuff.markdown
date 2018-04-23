---
layout: post
title:  "More excitement learning Loaders"
date:   2018-04-22 18:42:58 -0500
categories: Android development
---


To understand this lesson we need to make sure we understand how load managers work. `LoaderManager` has three methods `onCreateLoader()`, `onLoadFinished`, `onLoadReset()`. 

![Loader, LoadManager and Activity Diagram]({{ "/assets/loader_diagram.png" }})

This exericise is working with the loadManager to cache data in the `onLoadFinish()` 

# The `deliverResults()`

The `deliverResults()` is an intermediary step between the background loading and the UI threads callback `onLoadFinished`. We override `deliverResults()` and cache the query results so it is availaible to us if the app status changes and we are forced to restart/resume.
