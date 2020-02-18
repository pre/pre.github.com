# Test from Github

Hello World

1
{% include _includes/hello.md %}

2
{% capture my_include %}{% include hello.md %}{% endcapture %}
{{ my_include | markdownify }}

3
{% capture another_include %}{% include _includes/hello.md %}{% endcapture %}
{{ another_include | markdownify }}
