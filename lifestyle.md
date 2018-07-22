---
layout: page
title: Lifestyle
permalink: /lifestyle/
order: 1
---
                


Hi, this is where I talk about some of my unusual approaches to navigating life.


{% if site.posts.size > 0 %}
    
{% for post in site.categories.Lifestyle %}
            
{% assign date_format = site.minima.date_format | default: "%b %d, %Y" %}
{{ post.categories | join: ' ' }}  <span class="post-meta"> - {{ post.date | date: date_format }}</span> 
                
<a class="post-link" href="{{ post.url | relative_url }}">
{{ post.title | escape }}
</a>
                
{{ post.excerpt }}
                
            
{% endfor %}
    
    
{% endif %}              
        
