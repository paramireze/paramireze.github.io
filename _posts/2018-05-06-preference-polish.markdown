---
layout: post
title: "Use Shared Preferences to load Preference Settings"
date: 2018-05-06 08:34:00 -0600
categories: "Android development"
---

In this exercise, we remove the hardcoded preference setting in `xml/pref_general.xml` file so `SharedPreferences` API will load the users selected preference location. We are able to accomplish this goal by using the `SharedPreferenceChangeListener` which will detect when a user has made a change to their preference location setting. Then, if there is a change, we call the Forcast Adapter to query the weather info and refresh the activity.

As I complete these activities, I am finding that I get confused when it comes to identifying the various class, interfaces and API's. The framework tucks those things nicely away somewhere and you only have to implement and call their methods. For this post, I would like to try and organize my understanding of those api's, classes and interfaces.

1. Preference Manager - from what I am reading, it is the interface that communicates between the `PreferenceActivity` and `SharedPreferences`. It is the glue that connect the `SharedPreferences` with the android `activity`. `Preference Manager` is a good resource for handling setting and retrieving default values.

2. Shared Preferences - this is the interface that provides methods that will do `CRUD` operations on the file system.

3. Preference Object - object used to create the ui preference for a preference activity. The preference key will be stored in `sharedPreference`.

 
