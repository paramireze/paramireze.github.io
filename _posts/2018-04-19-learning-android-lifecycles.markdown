---
layout: post
title:  "Introduction of Activity Lifecycles"
date:   2018-04-18 20:42:58 -0500
categories: Android development
---

One thing that never occured to me until this lesson, is how much mobile apps must constantly be changing states. When dealing with web applications, a user session is stored in a browser until closed or whatnot. 

It makes sense to me that the state of an mobile app must always be ready to conserve resources. I didn't realize that when a user rotates their screen, the entire app is `reStarted()`. To help manage resources, android uses several methods



{% highlight ruby %}


- onCreate()
- onStart()
- onResume()
- onPause()
- onStop()
- onDestroy()

{% endhighlight %}

Each of these methods are called depending on the user interaction with their device.

In the latest exercis, we learned how to use the `saveInstanceState()` which will save state information with a collection key-value pairs after the `onPause` and before `onStop()` method call. 

In our exercise, we override the `saveInstanceState()` to store query results so that if the user rotates their screen, they do not lose their data. 
Diagram showing lifecycle.

![this is a diagram about lifecycles and stuff!]({{ "https://snag.gy/fjncas.jpg" }})

