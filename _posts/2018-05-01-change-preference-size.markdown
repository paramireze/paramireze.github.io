---
layout: post
title: "Fun with Edit Text Preference"
date: 2018-05-01 07:31:01 -0600
categories: Android development
---

It has been a challenge understanding some of the `Preference` concepts that are being taught in this exercise. For example, we use the `PreferenceScreen` in our XML file. However, when I look up the documentation trying to understand exactly what it does, it says 

> `Represents a top-level Preference that is the root of a Preference hierarchy. A PreferenceActivity points to an instance of this class to show the preferences`

The documentation doesn't say much else and I am not able to see what the preference hierarchy looks like.

{% highlight ruby %}

<PreferenceScreen xmlns:android="http://schemas.android.com/apk/res/android">

    <EditTextPreference
        android:defaultValue="@string/pref_size_default"
        android:key="@string/pref_size_key"
        android:title="@string/pref_size_label" />


    <!-- COMPLETED (1) Add and EditTextPreference with all of the appropriate strings stored in strings.xml.
        It should have a key, default value of 1 and title -->

    <ListPreference
        android:defaultValue="@string/pref_color_red_value"
        android:entries="@array/pref_color_option_labels"
        android:entryValues="@array/pref_color_option_values"
        android:key="@string/pref_color_key"
        android:title="@string/pref_color_label" />

</PreferenceScreen>

{% endhighlight %}

In this exercise, we made an editable text box using `EditTextPreference`. It will display an edit box to the user and whatever value they enter will be stored in `SharedPreference`. 

# Edit Text Preference Screenshot
![Screenshot]({{ "/assets/edit_text_screenshot.png" }})

I found a nifty diagram which is close to ones I made in the past. It shows how an activity can inject a fragment into an activity to create a more <jargony word> modularized </jargony word> UI panes


# Preference Fragment Workflow Diagram

![Fragment Workflow Diagram]({{ "/assets/android-fragments-activity.png" }})

The `onSharedPreferenceChanged` is a listener that will detect changes being made by the user. It will receive and update the activity with those settings. 
 
# Shared Preferences API
![Shared Preference Diagram]({{ "/assets/shared_preference_diagram.png" }})

There are a lot of moving parts. I do see the value of having the `Preferences` API, however, it can be a bit of a black box. There is not a lot of documentation explaining how the various parts work. Perhaps I am just inexperienced and will figure it out someday. 
