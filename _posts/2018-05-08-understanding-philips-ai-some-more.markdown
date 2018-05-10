---
layout: post
title: "Java's JPA" 
date: 2018-05-08 12:30:50 -0500
categories: Philips Bridge
---

Hibernate in 2003 introduced the concept of abstract SQL and had the java world thinking in terms of persisting objects. Unfortunately, hibernate tightly coupled code to the database communication making it difficult for the use of other persistant technologies. 

Hibernate, among other ORM technologies, worked with the JCP (Java Community Process) to create a standard for communications for persisting data. As a aresult, a generic persistence API was created which resulted in the JPA 1.0 (2006) and then JPA 2.0 (2009). 

Creating the generic persistence API solved the problem of data persistence being tied to a specific technology. 

To answer the question, "what is JPA?", it is a specification that set guidelines for communications through the use of protocols, standards, and naming conventions. 

