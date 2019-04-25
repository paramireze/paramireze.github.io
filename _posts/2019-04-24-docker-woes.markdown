---
layout: post
title: "How I lost my insanity and almost got it back"
date: 2019-04-24 08:50:00 -0500
categories: Docker
---

I have been working on a ruby rails app and ran into a peculiar problem using Docker.
Whenever I tried to add a gem, I would run `docker-compose run web bundle install` and I would get the error message,

<img src='/assets/images/2019/april/docker_error.png' alt="Error Message" />

The log, after running the bundle install command, showed that it installed 

<img src='/assets/images/2019/april/docker_noko.png' alt="says installed" />

However, it was not saving. To solve this problem I had to run `bundle install` inside the container :/
