---
layout: page
title: Projects you can build with snap:bit
---

We prepared a list of projects for you to start tinkering with snap:bit. Snap:bit brings together Snap Circuits and the BBC micro:bit in a completely new learning experience.

The first projects are light and easy, aimed to introduce you to using snap:bit. Then we dive into more exciting projects, derived from real-life use cases.

### Basic lessons

These include basic instructions on how to properly connect Snap Circuits components to snap:bit. The projects involve little to no coding with the micro:bit.

{% for project in site.projects %}{% if project.category == 'lesson' %}
- [{{ project.title }}]({{ project.url }}){% endif %}{% endfor %}

### Projects

These are more complex projects that involve significantly more coding than the basic lessons. In fact, lots of projects share the same circuit diagram, but it is different code in the micro:bit, that makes them behave in a completely different way. This is the magic of software programming!

{% for project in site.projects %}{% if project.category == 'project' %}
- [{{ project.title }}]({{ project.url }}){% endif %}{% endfor %}
