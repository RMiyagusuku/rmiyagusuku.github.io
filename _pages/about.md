---
permalink: /
title: "About me"
excerpt: "About me"
author_profile: true
classes: wide
redirect_from: 
  - /about/
  - /about.html
---

I am an associate Professor at the [Instrumentation and Robotics Laboratory](https://www.ir.utsunomiya-u.ac.jp/), Utsunomiya University, working on robotics and robotic applications to agriculture, construction, and last-mile delivery. 

My research interests lie in Robotics, Sensor Fusion and Machine Learning.

All my code including ROS packages are available at my github

### Latest News 
---
<p style="font-size:10pt;">
{% assign news_ = site.news | reverse %}
{% for news in news_ limit:10 %}
<b>{{ news.date | date: "%Y-%m-%d" }}</b> &nbsp;&nbsp; {{ news.excerpt | markdownify | remove: '<p>' | remove: '</p>' }} &nbsp; <a href='{{ news.permalink }}'><b>More</b></a><br/>
{% endfor %}
</p>
