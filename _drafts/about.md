---
layout: page
title: About
permalink: /about/
example: Example text in this variable. More example text.
---

This page describes the amazing {{ site.title }} by {{ site.author.name }}.

Here is a variable: {{ page.example }}

{% include big-cat.html %}

## About About Pages

The About page is a common convention found on websites.
It is your opportunity to let us know all the details "about" your project:

- focus and topic area
- people involved
- code and projects used

{% for animal in site.data.animals %}
- The {{ animal.name }} is a {{ animal.size }} animal.
{% endfor %}



## Large animals are best!

{% for animal in site.data.animals %}
{% if animal.size == "large" %} - <strong style="color: {{ animal.colour }};">{{ animal.name }}</strong>
{% else %} - <small>{{ animal.name }}</small>
{% endif %}
{% endfor %}


## Small animals only

{% assign small_animals = site.data.animals | where: "size", "small" %}
{% for animal in small_animals %}
- {{ animal.name | upcase }}
{% endfor %}

