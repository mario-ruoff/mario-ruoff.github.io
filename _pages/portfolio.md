---
title: Projects
layout: archive
permalink: /portfolio/
author_profile: true
---

{% include base_path %}

{% for post in site.portfolio reversed %}
    {% include archive-single-portfolio.html type="grid" %}
{% endfor %}
