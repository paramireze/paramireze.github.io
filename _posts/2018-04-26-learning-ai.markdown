---
layout: post
title: "Some gotchas working with Philips AI"
date: 2018-04-26 18:16:01 -0600
categories: Ruby Rails development
---

# No dbConsole or migrations
for me, this is a huge change in workflow. Straight ruby rails development is heavily integrated in the command line. However, AI uses `rails 4.2.0`, one major behind, with a `java/hibernate OOM`. This means that a lot of the terminal functionality is lost such as `dbconsole`. 




