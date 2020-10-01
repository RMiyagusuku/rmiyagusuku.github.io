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

I am an assistant Professor at the [Measurement and Robotics Laboratory](https://www.ir.utsunomiya-u.ac.jp/), Utsunomiya University, working with Prof. Koichi Ozaki on robotics and robotic applications to agriculture. 

I am also a visiting researcher at the University of Tokyo, working with Prof. Hajime Asama and Prof. Atsushi Yamashita on [service robotics](http://www.robot.t.u-tokyo.ac.jp/asamalab/en/). 

My research interests lie in Robotics, Sensor Fusion and Machine Learning.

All my code including ROS packages are available at my github


### Latest News
---
{% assign i = 0 %}
<p style="font-size:10pt;"> 
{% for row in site.data.news %}
  {% if row["Status"] != "Updated" and i < 10 %} 
  {% assign i = i | plus:1 %}
  <b>{{ row["Date"] }}</b> &nbsp;&nbsp; {{ row["Info"] }} <br/>
  {% endif %}
{% endfor %}
</p>


### Latest News 
---
<p style="font-size:10pt;">
{% for news in site.news reversed %}
<b>{{ news.date | date: "%Y-%m-%d" }}</b> &nbsp;&nbsp; {{ news.excerpt | markdownify | remove: '<p>' | remove: '</p>' }} &nbsp; <a href='{{ news.permalink }}'><b>More</b></a>
{% endfor %}
</p>