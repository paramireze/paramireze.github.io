---
layout: post
title: "A New App"
date: 2019-03-21 12:00:00 -0500
published: false
categories: Ruby Rails development
---

I am building a ruby rails app to replace an existing php application.
The app answers the question "why do you deserve to be paid?"
It is a place for faculty to document their contributions to research and education to the University. 
Reviewers will then go over their entries and assign RVU (relative value units) to each entry.

Diagramming is to software development as blueprints are to construction/architecture 
   
![erd diagram]({{ '/assets/images/2019/march/faf-models.png' }})

For this particular application, I am de-normalizing the tables a bit to simplify the relations.
I could create a category_questions table, however, creating questions is inexpensive.
The problem with the existing FAF is it is over designed and can be over-welming for anyone not accustomed to the application.

For this app, I am taking a test driven development approach.
My goal will be to make a fully tested application from start to finish

# TDD Concepts

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
