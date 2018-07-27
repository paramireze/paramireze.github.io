---
layout: post
title: "Persisting Data"
date: 2018-07-24 10:00:00 -0500
categories: iOS Development
---

I will be persisting the Meal class data using the `NSCoding` protocol. I subclass the `NSObject` to override the `encordeWith` methods.

# step 1: implement encodeWithCoder method
the `encodeWithCoder` allows for class information to be archived. 
The encode method takes the property name and value and stores it using a unique key for reference.

# step 2: create init method to decode/encode
There is a lot going on in the next block of code so I left comments within the block code to help me figure out what is happening

{% highlight ruby %}
required convenience init?(coder aDecoder: NSCoder) {
    # required      - enforces this methods implementation in all subclasses
    # convenience   - secondary initializer. Must call a designated initializer
    # init?         - failable initializer which means it can return nil
    
    # enforce required and valid data using type casting and guard statements
    guard let name = aDecoder.decodeObject(forKey: PropertyKey.name) as? String else {
        # guard         - all conditions must be met
        # as?           - optional type casting. In this statement, it tries to convert the name property into a string
        # decodeObject  - checks if key exists and returns false if nil
    }
    
    # Because photo is an optional property of Meal, just use conditional cast.
    let photo = aDecoder.decodeObject(forKey: PropertyKey.photo) as? UIImage
    
    let rating = aDecoder.decodeInteger(forKey: PropertyKey.rating)
    
    # Must call designated initializer.
    self.init(name: name, photo: photo, rating: rating)
}
{% endhighlight %}

# step 3: find a place to store data
I defined static variables to define the file system path. `Static` means that it is unchanging no matter how many instances are created.



