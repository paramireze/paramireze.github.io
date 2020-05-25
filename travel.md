---
layout: page
title: Reviews
permalink: /reviews/
order: 3
---              

{% if site.posts.size > 0 %}
    
{% for post in site.categories.Review %}
            
{% assign date_format = site.minima.date_format | default: "%b %d, %Y" %}
{{ post.categories | join: ' ' }}  <span class="post-meta"> - {{ post.date | date: date_format }}</span> 
                
<a class="post-link" href="{{ post.url | relative_url }}">
{{ post.title | escape }}
</a>
                
{{ post.excerpt }}              
            
{% endfor %}
    
    
{% endif %}              
        
