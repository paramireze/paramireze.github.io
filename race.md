---
layout: page
title: Races
permalink: /race/
order: 4
---

![bike race]({{ "/assets/images/2018/aug/bike.JPG" }})

{% if site.posts.size > 0 %}
    
{% for post in site.categories.Race %}
            
 
                
<a class="post-link" href="{{ post.url | relative_url }}">
    {{ post.title | escape }}
</a>

{% assign date_format = site.minima.date_format | default: "%b %d, %Y" %}

{{ post.categories | join: ' ' }}  <span class="post-meta"> - {{ post.date | date: date_format }}</span>
                
{{ post.excerpt }}
<hr />                
             
{% endfor %}
    
    
{% endif %}              
        
