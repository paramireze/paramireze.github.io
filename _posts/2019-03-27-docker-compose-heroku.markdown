---
layout: post
title: "A New App"
date: 2019-03-21 12:00:00 -0500
categories: Ruby Rails development
---

I am building a ruby rails app to replace an existing php application.
It is a Question/Answer application that allows faculty to document productivity.
Reviewers will then go over their entries and either approve or deny their entries.

The first thing I do with any new application is diagram.
Visualizing the data models will allow me to have a source of truth when many hours in coding.

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
