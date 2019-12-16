---
layout: default
title: Home
---
# Schismatic

---
## Roadmap

* Add redux idioms and basics
* Move pinouts pictures over from onenote
* go through onenote to check it out
* it's ok to add just links to things for tutorials, no need to copy things over and reexplain

{% assign pages = site.pages | where: 'layout', 'page' | sort: 'path' %}
{% assign last = '' %}
{% for p in pages %}
	{% assign splitPath = p.path | split: '/' %}
	{% assign name = splitPath | slice: -2, 1 | first | capitalize %}
	{% assign path = p.path | remove_first: p.name %}
	{% assign current = splitPath | slice: 1 %}
	{% if current != last %}
---
### {{current}}
	{% endif %}
* [{{name}}]({{path}})
	{% assign last = splitPath | slice: 1 | 0, -1 %}
{% endfor %}
