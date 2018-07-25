---
layout: page
title: Travel
permalink: /travel/
order: 3
---
                
Hi, this is where I talk about travel and adventuring

{% if site.posts.size > 0 %}
    
{% for post in site.categories.Travel %}
            
{% assign date_format = site.minima.date_format | default: "%b %d, %Y" %}
{{ post.categories | join: ' ' }}  <span class="post-meta"> - {{ post.date | date: date_format }}</span> 
                
<a class="post-link" href="{{ post.url | relative_url }}">
{{ post.title | escape }}
</a>
                
{{ post.excerpt }}              
            
{% endfor %}
    
    
{% endif %}              
        
