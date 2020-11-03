---
layout: archive
title: "Workshops"
permalink: /workshops/
author_profile: true
---

List of workshops with resources.

{% include base_path %}

{% for post in site.workshops reversed %}
  {% include archive-single.html %}
{% endfor %}