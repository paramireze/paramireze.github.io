---
layout: post
title:  "L2 Java"
date:   2018-04-19 08:00:58 -0500
categories: Android development
---
# Final,Void, Static

The first thing I am noticing when learning Java is all the various declaration types when it comes to variables, constants, methods and functions. I am use to weakly typed languages like PHP and javascript where programmers can easily code in jibberish.

I see `public`, `private`, `protected` being used and remember well from my education how they are used. However, I do not understand `final`, `void`, `static`. 

- `static`: only one variable instance exists for all objects. They share the variable
 
- `final`: the value cannot be changed after it is intialized. Also known as a constant

- `static final`: means only one instance of the variable no matter how many classes are built.  

- `void`: no return value! so simple and yet so foreign

# Anonymous Inner Class

I am stuck again. I am trying to learn about android aSyncTaskLoader and can't get past Anonymous Inner Classes. I have no way of learning more advanced concepts without understanding the basics of Java OOD. 

Anonymous inner classes are useful in writing implementation classes for listener interfaces in graphics programming. A top voted answer on stackoverflow says he uses `anonymous inner classes` to attach event handlers and only for one-offs. Otherwise, he recommends making a separate class that implements

{% highlight ruby %}

* Single object is created without a name
* Useful for making an instance of an object for extras such as overloads
* Avoid creating a subclass

{% endhighlight %} 

![Anonymous Inner Class Diagram]({{ "/assets/images/2018/jan-june/inner_classes.jpg" }})



