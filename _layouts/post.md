---
layout: default
---

{{ content }}

<hr>

<section class="page-navigation">
  <div class="previous-page">
    {% if page.previous %}
        &laquo; 
        <a href="{{ page.previous.url }}">
          {{ page.previous.title }}
        </a>
    {% endif %}
  </div>
  
  <div class="next-page">
    {% if page.next %}
      <a href="{{ page.next.url }}">
        {{ page.next.title }}
      </a>
      &raquo;
    {% endif %}
  </div>
</section>
