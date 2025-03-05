---
layout: single
title: Publications
permalink: /publications/
author_profile: true
---

## Preprints
{% assign preprints = site.publications | where: "category", "preprints" | sort: "date" | reverse %}
{% for publication in preprints %}
  <p><strong>{{ forloop.index }}. {{ publication.title }}</strong></p>
  <p><strong>Authors:</strong> {{ publication.authors }}</p>
  <p><strong>Venue:</strong> {{ publication.venue }}</p>
  <p><a href="{{ publication.url }}">More Info</a></p>
{% endfor %}

## Journal Articles
{% assign journal_papers = site.publications | where: "category", "journal" | sort: "date" | reverse %}
{% for publication in journal_papers %}
  <p><strong>{{ forloop.index }}. {{ publication.title }}</strong></p>
  <p><strong>Authors:</strong> {{ publication.authors }}</p>
  <p><strong>Venue:</strong> {{ publication.venue }}</p>
  <p><a href="{{ publication.url }}">More Info</a></p>
{% endfor %}



