---
layout: default
title: Home
---
# Schismatic

{% for page in site.pages %}
  {% if page.layout == 'page'%}
	{% assign splitPath = page.path | split: '/' %}
	{% assign name = splitPath[1] | capitalize %}
	{% assign path = splitPath[0] | append: '/' | append: splitPath[1] %}
[{{name}}]({{path}})
  {% endif %}
{% endfor %}
