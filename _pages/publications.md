---
layout: default
title: Publications
permalink: /publications/
---

# Publications

<ul>
{% for publication in site.publications %}
  <li>
    <h2>{{ publication.title }}</h2>
    <p><strong>Venue:</strong> {{ publication.venue }}</p>
    <a href="{{ publication.url }}">More Info</a>
  </li>
{% endfor %}
</ul>
