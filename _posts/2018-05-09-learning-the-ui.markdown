---
layout: post
title: "Basic iOS UI Design Principles"
date: 2018-05-09 07:20:50 -0500
categories: iOS Development 
---

In this lesson, we use `XCodes` object library to drag and drop a button. We then set the background through the attributer editor on the right side of the IDE. These concepts are straight forward and important and may be a bit dull for those who are knowlegable of UI design.

### auto layout
We are able to position elements on the page using constraints. Once defined, weare then able to control how the element is positioned and sized on different devices. We are able to create constraints by clicking the `add a constraint` button while the element is highlighted. 

### Johny Ive
Johny Ive is the senior vice president of technology and design for Apple. He is a british designer who is currently the the Chancellor of the Royal College of Art in London. He worked closely with Steve Jobs many years ago and was a major influence on the Macbook design. 

Some other notable of Johny's is his Apple Store design in New York City which is made of plexiglass and Durable Cable. Johny was heavily influenced by german industrial designer Dieter Rams who is known for less but better design philosophy. 

super useful diagram
![Leadership Diagram]({{ "/assets/ios/johny_ive.png" }}) 

### Interface Builder

interface builder is a way to drag and drop html elements and form fields. Interface builder can use `IBAction` and `IBoutput` to link UI elements to your code.

### Target Action

Target Action is a design pattern that allows objects to dynamically build their relationships. This has the advantage of allowing objects to build their relationships at run time. Design pattern is a re-usable solution to a reoccuring problem in software design. 

Using XCode, we are able to create a target-action through the use of `@IBaction`. by control-click the `record` button and dragging a pointer to the ViewController. 

### Run-Time 

Warning: i went down a rabbit hole of things I kind of understood, however, never took the time to really understanding them. Reading about Runtime, interpreters, compilers and translaters taught me that I know very little about the meaning behind many of the words used in my industry.

`Run-time` is also known as an interpreter. It is a program that takes human readable code and converts it into machine language. A `compiler`

1. machine code = binary
2. high-level langauge = human readable code (php,java,ruby,etc)
3. Source code = code written in high-level language

Compilers and interpreters convert high level language and converts it into machine code


### Translater vs Compiler

An `intrerpreter` converts a program on statement at a time. It will also stop execution when it hits an error. Programming languages like python and ruby uses interpreters.

a `compiler` scans the entire program and translates it as a whole into machine code. generates errors after compiling, making debuging more difficult. programs like C, C++ use compilers.

 

