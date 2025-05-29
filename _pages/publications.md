---
layout: single
title: Publications
permalink: /publications/
author_profile: true
---

<h2 class="preprint-heading">Preprints</h2>
{% assign preprints = site.publications | where: "category", "preprints" | sort: "date" | reverse %}
{% for publication in preprints %}
  <div class="publication-entry">
    <p><strong>{{ forloop.index }}. {{ publication.title }}</strong></p>
    <p><strong>Authors:</strong> {{ publication.authors }}</p>
    {% if publication.eprint %}
      <p><strong>arXiv:</strong> <a href="https://arxiv.org/abs/{{ publication.eprint }}" target="_blank">{{ publication.eprint }}</a></p>
    {% endif %}
    {% if publication.doi %}
      <p><strong>DOI:</strong> <a href="https://doi.org/{{ publication.doi }}" target="_blank">https://doi.org/{{ publication.doi }}</a></p>
    {% endif %}
  </div>
{% endfor %}

<h2 class="journal-heading">Journal Articles</h2>
{% assign journal_papers = site.publications | where: "category", "journal" | sort: "date" | reverse %}
{% for publication in journal_papers %}
  <div class="publication-entry">
    <p><strong>{{ forloop.index }}. {{ publication.title }}</strong></p>
    <p><strong>Authors:</strong> {{ publication.authors }}</p>
    <p><strong>Published in:</strong> {{ publication.venue }}</p>
    {% if publication.published %}
      <p><strong>Published:</strong> {{ publication.published }}</p>
    {% endif %}
    {% if publication.eprint %}
      {% assign arxiv_id = publication.eprint | split: ' ' | first | remove: 'arXiv:' %}
      <p><strong>arXiv:</strong> <a href="https://arxiv.org/abs/{{ arxiv_id }}" target="_blank">{{ arxiv_id }}</a></p>
    {% endif %}
    {% if publication.doi %}
      <p><strong>DOI:</strong> <a href="https://doi.org/{{ publication.doi }}" target="_blank">https://doi.org/{{ publication.doi }}</a></p>
    {% endif %}
  </div>
{% endfor %}




