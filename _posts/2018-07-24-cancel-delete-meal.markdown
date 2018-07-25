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


## Deleting Reviews

Use delegates to make direct updates to the tableview

# step 1: allow edit mode
tableView provides the `editButtonItem`. When pressed, it will start an edit mode and present `-` signs for each row.

# step 2: add delete functionality
To be able to edit/delete a particular row in the tableview, we need to overload the `tableview` method and pass in an additional argument that is used to referenced to the selected row.

