---
layout: post
title: "Adding Preference Validation"
date: 2018-05-02 07:10:01 -0600
categories: Android development
---

I learned that android has easy ways of handling validation using the interface `OnPreferenceChangeListener`. Basically, users are forced to enter a valid number since we are able to check their input before the application submit their changes.

# Workflow diagram
This diagram shows how the SettingsFragment assigns the listener to `TextEditPreference` and validates user input in the `OnPreferenceChange` 



![visualizer screen]({{ "/assets/images/2018/jan-june/validation_diagram.png" }})
