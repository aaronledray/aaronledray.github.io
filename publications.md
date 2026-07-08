---
layout: page
title: "Publications"
permalink: /publications/
---



<h1 style="text-align: center;">Publications</h1>
<hr>

{% for pub in site.data.publications %}
{% assign journal = pub.journal | default: "" | strip %}
  {% assign status = pub.status | default: "" | strip %}
  {% assign year = pub.year | default: "" | strip %}
  {% assign volume = pub.volume | default: "" | strip %}
  {% assign pages = pub.pages | default: "" | strip %}
  {% assign pmid = pub.pmid | default: "" | strip %}
{% assign link = pub.link | default: "" | strip %}
- **{{ pub.title }}**  
  {{ pub.authors }}  
  {% if journal != "" %}_{{ journal }}_{% if year != "" %}, {{ year }}{% endif %}{% if volume != "" %}, Vol. {{ volume }}{% endif %}{% if pages != "" %}, pp. {{ pages }}{% endif %}{% if pmid != "" %}  
  [PubMed](https://pubmed.ncbi.nlm.nih.gov/{{ pmid }}){% endif %}{% if link != "" %}{% if pmid != "" %} | {% else %}  {% endif %}[Link]({{ link }}){% endif %}{% endif %}
  {% if status != "" %}  
  _{{ status }}_{% endif %}
{% endfor %}

---

[View on Google Scholar](https://scholar.google.com/citations?user=zpRylnEAAAAJ&hl=en&oi=ao)
