---
layout: default
---

{{ content }}

<hr>

{% if page.next %}
  Next: 
  <a href="{{ page.next.url }}">
    {{ page.next.title }}
  </a>
{% endif %}

<br>

{% if page.previous %}
  Previous: 
  <a href="{{ page.previous.url }}">
    {{ page.previous.title }}
  </a>
{% endif %}
