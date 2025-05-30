---
layout: single
title: Publications
permalink: /publications/
author_profile: true
---

<h2 class="preprint-heading">Preprints</h2>
{% assign preprints = site.publications | where: "category", "preprints" | sort: "date" | reverse %}
{% for publication in preprints %}
  <div class="publication-card">
    <p class="pub-title"><strong>{{ forloop.index }}. {{ publication.title }}</strong></p>
    <p class="pub-meta">
      {{ publication.authors }}<br>
      {% if publication.eprint %}
        arXiv: <a href="https://arxiv.org/abs/{{ publication.eprint }}" target="_blank">{{ publication.eprint }}</a><br>
      {% endif %}
      {% if publication.doi %}
        DOI: <a href="https://doi.org/{{ publication.doi }}" target="_blank">{{ publication.doi }}</a><br>
      {% endif %}
    </p>
  </div>
{% endfor %}

<h2 class="journal-heading">Journal Articles</h2>
{% assign journal_papers = site.publications | where: "category", "journal" | sort: "date" | reverse %}
{% for publication in journal_papers %}
  <div class="publication-card">
    <p class="pub-title"><strong>{{ forloop.index }}. {{ publication.title }}</strong></p>
    <p class="pub-meta">
      {{ publication.authors }}<br>
      {% if publication.venue %}
        Published in: {{ publication.venue }}<br>
      {% endif %}
      {% if publication.published %}
        Published: {{ publication.published }}<br>
      {% endif %}
      {% if publication.eprint %}
        arXiv: <a href="https://arxiv.org/abs/{{ publication.eprint }}" target="_blank">{{ publication.eprint }}</a><br>
      {% endif %}
      {% if publication.doi %}
        DOI: <a href="https://doi.org/{{ publication.doi }}" target="_blank">{{ publication.doi }}</a>
      {% endif %}
    </p>
  </div>
{% endfor %}
