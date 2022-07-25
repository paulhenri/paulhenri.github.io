---
layout: page
title: Recipes
permalink: /recipes/
---

## Why such a section here ?
For a while now i have found it to be more and more difficult to simply look for a cooking recipe online.GPDR made things even more challenging... Recipes blogs have a lot of unwanted J.S, unwanted back-storry around the recipe and loading pages is now slower than 10 years ago...

I got inspired by [Luke Smith](https://lukesmith.xyz/) project called [Based Cooking](https://based.cooking/) and it's not impossible that some recipes will find their way to based.cooking

This section has no other way than storing recipes for me instead of storing them on a notebook or on some third-app application.

{% for cat in site.category-list %}
### {{ cat }}
<ul>
  {% for page in site.pages %}
    {% if page.resource == true %}
      {% for pc in page.categories %}
        {% if pc == "recipes" %}
          <li><a href="{{ page.url }}">{{ page.title }}</a></li>
        {% endif %}   <!-- cat-match-p -->
      {% endfor %}  <!-- page-category -->
    {% endif %}   <!-- resource-p -->
  {% endfor %}  <!-- page -->
</ul>
{% endfor %}  <!-- cat -->


