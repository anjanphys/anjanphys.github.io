---
layout: single
title: Publications
permalink: /publications/
author_profile: true
---

## Preprints
<ul>
{% assign preprints = site.publications | where: "category", "preprints" | sort: "date" | reverse %}
{% for publication in preprints %}
  <li>
    <h2>{{ forloop.index }}. {{ publication.title }}</h2>
    <p><strong>Authors:</strong> {{ publication.authors }}</p>
    <p><strong>Venue:</strong> {{ publication.venue }}</p>
    <a href="{{ publication.url }}">More Info</a>
  </li>
{% endfor %}
</ul>

## Journal Articles
<ul>
{% assign journal_papers = site.publications | where: "category", "journal" | sort: "date" | reverse %}
{% for publication in journal_papers %}
  <li>
    <h2>{{ forloop.index }}. {{ publication.title }}</h2>
    <p><strong>Authors:</strong> {{ publication.authors }}</p>
    <p><strong>Venue:</strong> {{ publication.venue }}</p>
    <a href="{{ publication.url }}">More Info</a>
  </li>
{% endfor %}
</ul>


