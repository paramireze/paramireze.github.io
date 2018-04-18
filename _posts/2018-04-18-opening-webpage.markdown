---
layout: post
title:  "Learning Intentions and Activities"
date:   2018-04-18 09:42:58 -0500
categories: Android development
---
Opening a webpage is simple right? It should be, at least in my experience as a developer it is. You have an ancor tag and the ancor tag will then allow the user to click and be on their merry. 

Android does it a little different and I am still learning why. In the tutorial, i had to create a button that when clicked would open up a webpage. Basically, I attached a method call to the button which would then execute the openWebPage function.

![Using Intents Diagram]({{ "/assets/openWebPage.jpeg" }})


My understanding of this tutorial is that android uses intents to do common tasks. In this specific tutorial, we use an intent to open a webpage. 

{% highlight java %}
public void openWebPage(String url) {
    Uri webpage = Uri.parse(url);
    Intent intent = new Intent(Intent.ACTION_VIEW, webpage);
    if (intent.resolveActivity(getPackageManager()) != null) {
        startActivity(intent);
    }
}
{% endhighlight %}

Intent does more than just sanity checks and validation. According to android docs "{% highlight bash %} Its most significant use is in the launching of activities, where it can be thought of as the glue between activities. It is basically a passive data structure holding an abstract description of an action to be performed. {% endhighlight %}


![Using Intents Diagram 2]({{ "/assets/intent-filters.png" }})
