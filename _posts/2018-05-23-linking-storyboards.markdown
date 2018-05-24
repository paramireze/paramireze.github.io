---
layout: post
title: "Linking Storyboards"
date: 2018-05-23 07:30:00 -0500
categories: iOS Development 
---

A segue is a way of linking two story boards together. For this application, I use a seque to transfer the audio session to the other storyboard. I use the `AVAudioRecorder` class to handle the recording logic by calling its methods inside the `recordButton` action. I then create a delegate that lets `AVAudioRecorder` know about the applications recording logic inside the view controller.

From what I have learned today, Delatation is a way for two objects to communicate with one another lettings one another know that they are finished with an action. In this case, we use a delegate to communicate between two viewController classes. We are able to do this using the AVAudioRecorderDelegate protocol and making sure we are conforming to their stands when it comes to implementing the protocol
