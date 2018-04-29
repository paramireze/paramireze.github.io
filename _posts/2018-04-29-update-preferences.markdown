---
layout: post
title: "Adjusting Settings on an Android App"
date: 2018-04-29 07:30:01 -0600
categories: Android development
---

Exercise 6.4 solves the problem of How can a person set preferences for a given app. To solve this problem we make a separate activity that allows a user to select or unselect a checkbox for displaying a specific settings. For this exercise, the specific setting is whether or not to show the bass circle while the app is playing music. 
 
![Home Page]({{ "/assets/show_bass_home.png" }})
![Settings Page]({{ "/assets/show_bass_pref.png" }})

to understand how we are able to track user preferences, we must first understand how the application activities are communicating. In the diagram below, we show the behavior of the app when it is created and the user clicks the settings link in the menu bar. The dotted lines indicate what happens when the user checks or unchecks the `Show Bass` checkbox. 

![Settings Activity Diagram]({{ "/assets/show_bass_diagram.png" }})

This lesson taught me to use the `SharedPreferencesListener` to track preference choices by the user. 
