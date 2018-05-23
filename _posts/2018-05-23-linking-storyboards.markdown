---
layout: post
title: "Linking Storyboards"
date: 2018-05-23 07:30:00 -0500
categories: iOS Development 
---

For my recording app, I created what is known as a seque that links two view controllers. Basically, a segue is a way of linking two story boards together. For this application, I want to use the seque to transfer the audio session to the other storyboard for non nafarious reasons. 

I use the `AVAudioRecorder` to handle the recording logic using its methods. I then create a delegate that will let `AVAudioRecorder` know about my own written action inside the Stop Recording View Controller.
