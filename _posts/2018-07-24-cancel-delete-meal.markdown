---
layout: post
title: "Cancel And Delete Functionality"
date: 2018-07-24 10:00:00 -0500
categories: iOS Development
---

# Step 1: Check if add or edit button clicked
because edit is a `modal seque` and the cancel button is a `push seque`,
I added logic within `cancel()` to detect which seque was used to navigate to the page.

# Step 2: to Dismiss or not to Dismiss
If `Modal Segue` then `dismiss()` else if `Push segue` then pop from navigation stack()

{% highlight ruby %}
if isPresentingInAddMealMode {
        dismiss(animated: true, completion: nil)
    }
    else if let owningNavigationController = navigationController{
        owningNavigationController.popViewController(animated: true)
    }
}
{% endhighlight %}