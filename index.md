# Test from Github

Hello World

{% include _includes/hello.md %}

{% capture my_include %}{% include hello.md %}{% endcapture %}
{{ my_include | markdownify }}

{% capture another_include %}{% include _includes/hello.md %}{% endcapture %}
{{ another_include | markdownify }}
