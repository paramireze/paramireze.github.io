---
layout: post
title: "Back to the basics"
date: 2018-05-02 19:46:01 -0600
categories: Android development
---

In this exercise, the tutorial had me add a Settings Activity and a link in the menu bar to that page. To achieve this goal, I did the following

1. Create `SettingsActivity`
2. Add activity_settings.xml that will eventually be used to add preference items to
3. Add the links to the menu xml files
4. in `MainActivity` override the `onOptionsItemSelected` method and attach an event handler to the settings Link so the application knows to `startActivity` on the `Settings` intent.

I learned I can organize how menu items display using the item property `OrderInCategory`. In this particular exercise, we set that property to equal 100, causing it to display below the other menu item.


{% highlight ruby %}

<item
        android:id="@+id/action_settings"
        android:orderInCategory="100"
        android:title="@string/action_settings"
        app:showAsAction="never"/>

{% endhighlight %}

![Settings Image]({{ "/assets/images/2018/jan-june/06_sunshine_settings.png" }})


I learned that `FrameLayouts` are used to block out an area on the screen to display a single item. `FrameLayout` uses a single item so it is able to scale well when using difference size screens


I learned that android allows users to add a default home button in the menu bar by setting `setDisplayShowHomeEnabled` property to true.


