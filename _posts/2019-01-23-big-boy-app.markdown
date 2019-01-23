---
layout: post
title: "Building My First Big Boy App"
date: 2019-01-06 08:00:00 -0500
categories: Ruby Rails development
---

For work, I built what I consider to be my first big boy application called `Tollbooth`. According to the about page, 

{% highlight ruby %}

Tollbooth is a centralized place for residents, fellows, and faculty to track exams & reports.

- view discrepancies for exams
- track interesting/notable exams using flags
- filter exams

{% endhighlight %}

## dashboard

When a user logs in, they are brought to a main dashboard. The dashboard is populated based on the user roles and which exams they have worked on.

![Table View]({{ '/assets/images/2019/jan/dashboard.png' }})

Users can optionally open an exam and see a side by side report comparison.

![Exam Data]({{ '/assets/images/2019/jan/exam.png' }})

## challenges

#### lot of data 
The app has a lot of data gonig through it and it has been tough keeping the speeds up. To solve some of the issues, I lazy load some of the exam/report data and use javascript to quickly open the exam Modal

#### old framework
I am using `philips performance bridge` tech stack to develop the app. It is a ruby rails based tech stack that uses the JPA to persist data.

Creating queries is a challenge due to limitations with the JPA and the data models having to communicate with multiple databases.

Using Gems was a challenge too since the ruby version is way behind and many plugins are not able to work.

#### lack of experience
This is my first ruby rails project and it showed. THere were times I had to refactor my work multiple times to make things more modular. 

Luckily, there is someone on my team that has ruby rails experience and is able to help through code review

## Lessons Learned

#### code review
I was too relaxed on the code review process and a lot of bugs got through.

#### sprint meetings
Having sprint meetings regularly was a huge help communicating work and expectations. Knowing that someone had eyes on my work made me feel more motivated to do a better job.

#### optimizing data
Working with millions of exam records forced me to rethink how I query data, especially when working with many joins within each query. In the future, I will make sure to put the extra work up front to best extract data so it can scale with time.

## conclusion
Building this app has been a lot of fun for me. I enjoy having ownership of a project that I can invest in. There is something to be said having decision making capabilities for a project and seeing it through from start to end.