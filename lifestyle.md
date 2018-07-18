---
layout: page
title: Lifestyle
permalink: /lifestyle/
---

<div class="home">
  
  <img src='/assets/images/profile/lifestyle.jpg' alt="me">
  <p>
  You are welcome to follow my journey to experience life through simplistic means.
  </p>

  {{ content }}

  {% if site.categories.LIFESTYLE.size > 0 %}
    <h2 class="post-list-heading">{{ page.list_title | default: "Posts" }}</h2>
    

    <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | relative_url }}">via RSS</a></p>
  {% endif %}

</div>