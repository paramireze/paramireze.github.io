---
layout: post
title: "Fun with Table Views"
date: 2018-07-11 19:00:00 -0500
categories: iOS Development 
---

`Table Views` can be a bit overwelming when first using them. There is a lot of inherited methods from `UITableViewController`, `UITableViewDelegate`, and `UITableViewDataSource`. I think the best way to think of table views is the same way as any other custom control. Basically, you are dynamically generating the table, rows, cells and defining a view(s) that go in each cell. So, all the crazy amount of methods made available are there to help with generating those fields which explains why there are so many. 

![show food reviews]({{ '/assets/ios/july/show_food_reviews.png' }})

The screenshot shows data that I created by initializing three `meal` objects using static, hard-coded property values. 


{% highlight ruby %} 

    //MARK: Private Methods
    private func loadSampleMeals() {
        
        let photo1 = UIImage(named: "meal1")
        let photo2 = UIImage(named: "meal2")
        let photo3 = UIImage(named: "meal3")

        guard let meal1 = Meal(name: "Caprese Salad", photo: photo1, rating: 4) else {
            fatalError("Unable to instantiate meal1")
        }

        guard let meal2 = Meal(name: "Chicken and Potatoes", photo: photo2, rating: 5) else {
            fatalError("Unable to instantiate meal2")
        }

        guard let meal3 = Meal(name: "Pasta with Meatballs", photo: photo3, rating: 3) else {
            fatalError("Unable to instantiate meal2")
        }

        meals += [meal1, meal2, meal3]
    }


{% endhighlight %}

Eventually, I will move away from the hard-coded property values and hook into a database initialize my `Meal` object that way.




