---
layout: post
title: "Decision Trees Continued"
date: 2018-09-21 09:00:00 -0500
categories: Machine Learning
---

After watching the instructional videos on decision trees, I realized that I understand the concepts but have a hard time explaining it. 
For this post, I will try to formulate a summerization of each key concepts we learned.

# Representation
Representation is the visual tree that you see. Each leaf node is a test and each branch represents the result of the test.


# ID3
is an algorithm that uses a top down approach. 
From what I understand, the algorithm will iterate over all the attributes and then calculate the entropy (information gained).

# Expressiveness of DTs
Decision trees can express any function of the input attributes.
The video demostrated this using binary classification which used truth tables.

# Bias of ID3
ID3 algorithm has an inductive bias of preferring shorter trees.

# Inductive Reasoning
Conclussions that are arrived at using the best evidence provided and not necessarily the complete or whole truth

# Overfitting
When an algorithm appears to explain a set of data well and able to predict future data sets, however, that is just appearance.
Overfitting can be tested against another data set outside of the data that is used for the algorithm. 
