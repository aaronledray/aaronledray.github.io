---
layout: page
title: "Publications"
permalink: /publications/
---



---

{% for pub in site.data.publications %}
- **{{ pub.title }}**  
  {{ pub.authors }}  
  _{{ pub.journal }}_, {{ pub.year }}{% if pub.volume %}, Vol. {{ pub.volume }}{% endif %}{% if pub.pages %}, pp. {{ pub.pages }}{% endif %}  
  [PubMed](https://pubmed.ncbi.nlm.nih.gov/{{ pub.pmid }}){% if pub.link %} | [Link]({{ pub.link }}){% endif %}
{% endfor %}

---

[View on Google Scholar](https://scholar.google.com/citations?user=zpRylnEAAAAJ&hl=en&oi=ao)
