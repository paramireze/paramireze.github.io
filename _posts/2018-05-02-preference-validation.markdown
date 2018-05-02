---
layout: post
title: "Adding Preference Validation"
date: 2018-05-08 07:10:01 -0600
categories: Android development
---

I learned that I can control validation from the user by implementing a `OnPreferenceChangeListener`. In the last exercise, we added a text input field so users are able to control the size of the visualizer bass, treble, and mid icons. 

# pref_visualizer.xml

{% highlight ruby %}

<PreferenceScreen xmlns:android="http://schemas.android.com/apk/res/android">

    <EditTextPreference
        android:defaultValue="@string/pref_size_default"
        android:key="@string/pref_size_key"
        android:title="@string/pref_size_label" />

</PreferenceScreen>

{% endhighlight %}


![visualizer screen]({{ "/assets/validation_preference.png" }})
![preference screen]({{ "/assets/validation_home.png" }})
