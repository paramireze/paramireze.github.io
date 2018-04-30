---
layout: post
title: "Adding a Pop up Menu for Preferences"
date: 2018-04-29 16:31:01 -0600
categories: Android development
---

My goal is to allow a user to modify the appication using preference settings. To achieve this goal, 

1. application must provide the user with form fields for selecting preferences 
2. make it so the application updates itself, reflecting the user selected changes. 

For the second point, this exercise teaches us to use `SharedPreferences` api to pass user selection to the main activity so it can update the application state using the new preference settings. The `SharedPreferences` api creates a file to store key->value pairs so it is available to other activities as well.


![Workflow Diagram]({{ "/assets/exercise-06-05-diagram-2.png" }})

It is good practice to use `Fragments` when creating UI Panes such as user preferences. `Fragments` are a sub-activity that has its own lifecycles. This is especially useful when creating a modular application since the activity has no outside dependencies to run its logic. 
