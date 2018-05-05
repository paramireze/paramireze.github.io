---
layout: post
title: "Customizing the Preferences for Weather App"
date: 2018-05-05 07:34:00 -0600
categories: "Android development"
---

In this exercise, we allow users to use preferences to determine where they want to get their weather data from. Much like previous exercises, we will be using the `SharedPreferences` api to handle storing and communicating data. Our jobs will be to correctly set up the files and call the well documented methods to do the work for us. 
 
![Location Preference]({{ "/assets/android/may/preference_diagram.png" }})

Looking at the image in the diagram, you will see the location isset to `Mountain View, CA 94043`. Where is the app getting that information from? Equally important is what happens when you change that location and click `ok`? In this post, we will be exploring that because that is the main focus of the exercise.

# where is the preference getting the location?

Well that is easy, it is the default string from `Strings.xml` :)

{% highlight ruby %}

    <!-- Default postal code for location preference [CHAR LIMIT=NONE] -->
    <string name="pref_location_default" translatable="false">Mountain View, CA 94043</string>

{% endhighlight %}

# what happens when the user updates the location? 
In the click event workflow diagram below, you see that the informaiton the user entered is sent to the `onSharedPreferenceChange` method inside the `SettingsFragment`. We set the preference settings using a method called `setPreferenceSummary()`.

![Location Click Workflow Diagram]({{ "/assets/android/may/preference_click_diagram.png" }})

All this is possible because we are using the `SharedPreferences` API which handles all the transfer and storage of data when the user is adding/updating preferences. 
