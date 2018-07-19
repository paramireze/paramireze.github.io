---
layout: page
title: Lifestyle
permalink: /lifestyle/
---
                
![paul avatar]({{ "/assets/images/profile/lifestyle.JPG" }})

{%- if site.posts.size > 0 -%}
    
{%- for post in site.categories.Lifestyle -%}
            
{%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
{{ post.categories | join: ' ' }}  <span class="post-meta"> - {{ post.date | date: date_format }}</span> 
                
<a class="post-link" href="{{ post.url | relative_url }}">
{{ post.title | escape }}
</a>
                
{{ post.excerpt }}
                
            
{%- endfor -%}
    
    
{%- endif -%}              
        
Hi, this is whwere I talk about stuff