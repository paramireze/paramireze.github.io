---
layout: post
title: "A New App"
date: 2019-03-21 12:00:00 -0500
categories: Ruby Rails development
---

I am building a ruby rails app to replace an existing php application.
The app answers the question "why do you deserve to be paid?
It is a place for faculty to document their contributions to research and education to the University. 
Reviewers will then go over their entries and either approve or deny their entries.

For me, diagramming is absolutely essential for understanding how to design an application.
It is the blueprints to how I will build the application.
For now, I am only making a entity relational diagram since I am building out the models and database first. 

![erd diagram]({{ '/assets/images/2019/march/faf-models.png' }})

For this particular application, I am denormalizing the tables a bit to simplify the relations.
I could create a category_questions table.
The problem with the existing FAF is it is over designed. It has a crazy database that is normalized to the 6nf.

For building this app, I am teaching myself how to do a test driven development approach.
Basically, I will write the tests before I write the code.
I have been told this is a more effecient way of developing in the long run by far.


Acceptance Test
- high level
- driven by user/customer
- going onto the website, add three items to shopping cart, making a purchase, test the credit card, etc

Unit Tests
- isolate very small component
- define the state of the application

RSpec vs mini-tests
- testing framework
- minitests are built in while RSpec is an extension
- some claim RSpec can handle more complex tasks

Capybara 
- dom interaction/manipulation
- web driver
- interpation of the website itself

Factory Girl
- dsl creating data within a database
- generating demo data

Shoulda Matchers
- associations

Database Center
