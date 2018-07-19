---
layout: page
title: Lifestyle
permalink: /lifestyle/
---
                
![paul avatar]({{ "/assets/images/profile/lifestyle.JPG" }})
  
{%- if site.posts.size > 0 -%}
    <ul class="post-list">
        {%- for post in site.categories.Lifestyle -%}
            <li>
                {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
                {{ post.categories | join: ' ' }}  <span class="post-meta"> - {{ post.date | date: date_format }}</span> 
                <h3>
                <a class="post-link" href="{{ post.url | relative_url }}">
                {{ post.title | escape }}
                </a>
                </h3>
                {{ post.excerpt }}
                <hr />
            </li>
        {%- endfor -%}
    </ul>
    
{%- endif -%}              
        