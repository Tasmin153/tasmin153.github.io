---
layout: archive
title: "Industry Experience"
permalink: /experience/
---

{% include base_path %}

{% for post in site.experience reversed %}
  {% include archive-single.html %}
{% endfor %}
