---
layout: post
title: "Understanding Ruby Rails Development using Philips AI"
date: 2018-05-07 08:40:50 -0500
categories: Ruby Rails development
---

Philips Analytic Bridge provides a data and development platform which allow Health Care instituations to collaborate data and software solutions. Bridge is able to take clinical systems and store their data into a normalized central database. Application developers then has the option to use their integrated ruby rails  technology stack for development. 

 
![rails framework diagram]({{ "/assets/rails/rails_framework_diagram.png" }})

To best understand Philips AI Bridge, I will take a look at each of the technologies being used and briefly summerize each. I am new to these technologies and figure a general understanding will prepare me for a more thorough understanding at a later time

# RabbitMQ
By default, all webrequests are done by a `brokerless model`. That is a term used when the browser sends a web request directly to a server. `RabbitMQ` is the middleman that handles communications between a browser and a server. 

`RabbitMQ` solves scalability issues. A message broker is able to create a queue and use other machines to handle processing. This takes pressure off of the web server itself which is especially useful when dealing with large amounts of traffic. 

Some requests, such as requests that deal with emails, do not need an immediate response from the web server. An administrator can configure their implementation of a message broker so that some requests are high priority than others. 

# Postgres
I have worked with Postgres before and understand some of the differences. I do application development. From what I have read it seems like that I will not notice a big difference between mysql and postgres other than syntax. Both database would handle the type of relational database structures that I am use to creating. I look forward to working more with `postgres` since it is a more supported, full featured technology than `mysql`. 

# Extract, Transform, Load

