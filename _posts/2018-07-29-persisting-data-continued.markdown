---
layout: post
title: "Persisting Data - continued"
date: 2018-07-24 10:00:00 -0500
categories: iOS Development
---

Last post, I was able to set up the Meal class to handle data persistence. 
I can now add controls that allow the user to interact with the data so their information is saved on their file system.


# create saveMeals and loadMeals method
In `MealTableViewController`, I used the  `NSKeyedArchiver.archiveRootObject` to persist and `NSKeyedArchiver.unarchiveObject` to get meal data.

# call the saveMeals 
I placed a `saveMeals` method in the `unwindSegue` method since that is called after a new meal is created. 
I also added a `saveMeals` method in the `tableView(:forRowsAt)` method since that is called during an edit operation.

# load the data
in the `viewDidLoad` method of the mealTableViewController file, I called the `loadMeals` method.
If meals exist then display, else load sample data.

# Reference
[Apple Development Tut]({{ 'https://developer.apple.com/library/archive/referencelibrary/GettingStarted/DevelopiOSAppsSwift/PersistData.html#//apple_ref/doc/uid/TP40015214-CH14-SW1' }})