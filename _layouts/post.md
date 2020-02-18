---
layout: default
---

{{ content }}

<hr>

<section class="page-navigation">
  {% if page.previous %} 
    &laquo; 
    <a href="{{ page.previous.url }}">
      {{ page.previous.title }}
    </a>
  {% endif %}
  
  {% if page.next %}
    <a href="{{ page.next.url }}">
      {{ page.next.title }}
    </a>
    &raquo;
  {% endif %}
</section>
