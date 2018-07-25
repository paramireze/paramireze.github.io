---
layout: post
title: "LLVM and Other Compilers"
date: 2018-05-12 06:50:50 -0500
categories: iOS Development 
---

The LLVM is made up of a set of open source project libraries. The major advantage the LLVM offers is the ability for the optimization logic to remain independant of the front/back end. This means that the front/back end technology can be changed, upgrade, improved, swapped, etc. It also means the LLVM compiler can evolve independantly without having to be held back by the limitations of front/backend technologies. 
 
![LLVM Optimizer]({{ "/assets/images/2018/may/compiler.png" }})


### The GCC and Front vs Back End Compiling

The Stages of Common Compilers

1. Frontend -> converts source code into `Common intermediate representation` (lowest level human-readable programming language)
2. Optimization -> eliminate and simplify
3. Target specific optimizations are performed and code/assembly is generated

The advantage to having those three stages is the compiler can used with other frontend (languages) and backend (target machines). 
