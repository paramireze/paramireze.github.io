---
layout: post
title:  "Introduction of Activity Lifecycles"
date:   2018-04-18 20:42:58 -0500
categories: Android development
---

Android has their own unique lifecycle when it comes to running an app. There are seven different methods/states that are used to help manage resources. 


{% highlight ruby %}


- onCreate()
- onStart()
- onResume()
- onPause()
- onStop()
- onDestroy()

{% endhighlight %}

</ul>

These are the various lifecycle states that any app can be in. They can happen multiple times depending on the users interactions. For example, if the user decides to check tinder and open a new window, then the app will execute the `onPause()` then `onStop()` methods.  

In the latest exercis, we learned how to use the `saveInstanceState()` which will save state information with a collection key-value pairs after the `onPause` and before `onStop()` 

okay fine, this is what we are learning

![this is a diagram about lifecycles and stuff!]({{ "https://snag.gy/fjncas.jpg" }})

