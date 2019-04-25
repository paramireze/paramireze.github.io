---
layout: post
title: "Designing Data Models"
date: 2019-04-06 12:00:00 -0500
categories: Ruby Rails development
---

The problem I am trying to solve is "How does a software application dynamically create forms and allow users to submit data?". 
In answer to the question, I will be creating a `category`, `question`, `response`, `answers` tables to do just that.

## work in progress 
not quite done yet, this is as far as I got as of today.

<img src='/assets/images/2019/april/erd-diagram.png' alt="Building a database" />

The advantage to having a data driven application, as opposed to static, is non-software developers can update the system through the use of forms that updates the questions being asked in the database.

Also, it is best practice to avoid static coding since the goal of any programmer, that is worth their salt, is to never have to change the source code once it is considered complete.
