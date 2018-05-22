---
layout: post
title: "iOS Audio Recording"
date: 2018-05-22 07:30:00 -0500
categories: iOS Development 
---

I added the recording functionality to the `recordAudio` action inside the viewController. I am able to easily do this using `AVFoundation`. `AVFoundation` is a framework specific for handling audiovisual media in iOS apps. As a developer, I can use `AVFoundations` built in classes, and the class methods to record, save and play audio recordings for my app.

{% highlight ruby %}
import AVFoundation

class ViewController: UIViewController {

    // MARK: Properties

    var audioRecorder: AVAudioRecorder!

    @IBAction func recordAudio(_ sender: AnyObject) {
        recordingLabel.text = "Recording in progress"
        stopRecordingButton.isEnabled = true
        recordButton.isEnabled = false

        let dirPath = NSSearchPathForDirectoriesInDomains(.documentDirectory,.userDomainMask, true)[0] as String
        let recordingName = "recordedVoice.wav"
        let pathArray = [dirPath, recordingName]
        let filePath = URL(string: pathArray.joined(separator: "/"))

        let session = AVAudioSession.sharedInstance()
        try! session.setCategory(AVAudioSessionCategoryPlayAndRecord, with:AVAudioSessionCategoryOptions.defaultToSpeaker)

        try! audioRecorder = AVAudioRecorder(url: filePath!, settings: [:])        
        audioRecorder.isMeteringEnabled = true
        audioRecorder.prepareToRecord()
        audioRecorder.record()
    }
}
{% endhighlight %}



## AVFoundation Concepts

### NSSearchPathForDirectoriesInDomains` 
creates a directory of search paths that the application can use to create the filePath. the `Filepath` is a parameter used to instantiate the `AVAudioRecorder` class


### AVAudioRecorder 
is a class that allows an application to use an iOS audio device. When the user clicks the record audio button, our action will provide the filepath location and the settings as parameters when instantiating the `AVAudioRecorder` class. Once instantiated, we then call its functions isMeteringEnabled(), preparedToRecord(), and record() to enable the recording functionality


