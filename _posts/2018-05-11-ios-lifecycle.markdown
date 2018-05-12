---
layout: post
title: "iOS Life Cycle"
date: 2018-05-11 09:20:50 -0500
categories: iOS Development 
---

There are three important methods when an application is compiling. 

## ExtraCredit

Listed are things I learned unrelated to the title of this post

### LLVM Compiler

The LLVM compiler is different from others because their compiler technology consists of a set of libraries. As a result, the LLVM compiler is able to handle problems that other compilers are not able to. `XCode` uses the `Clang front end` to parse the source code and then hands it off to LLVM's backend compiler which converts it to machine language.

The major advantage the LLVM offers is the ability for the optimization logic to remain independant of the front/back end. This means that the front/back end technology can be changed, upgrade, improved, swapped, etc. It also means the LLVM compiler can evolve as the other technologies do. 
![LLVM Optimizer]({{ "/assets/ios/may/compiler.png" }})


### The GCC and Front vs Back End Compiling

The Stages of Common Compilers

1. Frontend -> converts source code into `Common intermediate representation` (lowest level human-readable programming language)
2. Optimization -> eliminate and simplify
3. Target specific optimizations are performed and code/assembly is generated

The advantage to having those three stages is the compiler can used with other frontend (languages) and backend (target machines). 
