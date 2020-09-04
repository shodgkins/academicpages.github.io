---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}
{% include group-by-array collection=site.publications field="grouping" %}

{% for group in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  {% for post in posts reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
