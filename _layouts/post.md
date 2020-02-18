---
layout: default
---

{{ content }}

<hr>

<section class="page-navigation">
  {% if page.previous %}
    <div class="previous-page">
      &laquo; 
      <a href="{{ page.previous.url }}">
        {{ page.previous.title }}
      </a>
    </div>
  {% endif %}
  
  {% if page.next %}
    <div class="next-page">
      <a href="{{ page.next.url }}">
        {{ page.next.title }}
      </a>
      &raquo;
    </div>
  {% endif %}
</section>
