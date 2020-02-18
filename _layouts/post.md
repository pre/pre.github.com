---
layout: default
---

{{ content }}

<hr>

<section class="page-navigation">
  {% if page.previous %} 
    &laquo; 
    <a class="previous" href="{{ page.previous.url }}">
      {{ page.previous.title }}
    </a>
  {% endif %}
  
  {% if page.next %}
    <a class="next" href="{{ page.next.url }}">
      {{ page.next.title }}
    </a>
    &raquo;
  {% endif %}
</section>
