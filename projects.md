---
layout: page
title: Projects you can build with snap:bit
---

### Basic lessons
{% for project in site.projects %}{% if project.category == 'lesson' %}
- [{{ project.title }}]({{ project.url }}){% endif %}{% endfor %}

### Projects
{% for project in site.projects %}{% if project.category == 'project' %}
- [{{ project.title }}]({{ project.url }}){% endif %}{% endfor %}