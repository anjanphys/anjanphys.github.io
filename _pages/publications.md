---
layout: single
title: Publications
permalink: /publications/
author_profile: true
---

# Preprints
<ul>
{% for publication in site.publications %}
  {% if publication.category == "preprints" %}
    <li>
      <h2>{{ publication.title }}</h2>
      <p><strong>Venue:</strong> {{ publication.venue }}</p>
      <a href="{{ publication.url }}">More Info</a>
    </li>
  {% endif %}
{% endfor %}
</ul>


# Journal Articles
<ul>
{% for publication in site.publications %}
  {% if publication.category == "journal" %}
    <li>
      <h2>{{ publication.title }}</h2>
      <p><strong>Venue:</strong> {{ publication.venue }}</p>
      <a href="{{ publication.url }}">More Info</a>
    </li>
  {% endif %}
{% endfor %}
</ul>


