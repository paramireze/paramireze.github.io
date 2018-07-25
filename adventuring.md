---
layout: page
title: Adventuring
permalink: /adventuring/
order: 1
---
                


Fun stuff I sometimes do on weekends, usually involving bikes
<hr />

{% if site.posts.size > 0 %}
    
{% for post in site.categories.Adventuring %}
            
 
                
<a class="post-link" href="{{ post.url | relative_url }}">
    {{ post.title | escape }}
</a>

{% assign date_format = site.minima.date_format | default: "%b %d, %Y" %}

{{ post.categories | join: ' ' }}  <span class="post-meta"> - {{ post.date | date: date_format }}</span>
                
{{ post.excerpt }}
<hr />                
             
{% endfor %}
    
    
{% endif %}              
        
