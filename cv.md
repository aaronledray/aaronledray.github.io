---
layout: page
title: "Curriculum Vitae"
permalink: /cv/
---

# {{ site.data.cv.name }}

{{ site.data.cv.location }}  
{% if site.data.cv.phone %}{{ site.data.cv.phone }} • {% endif -%}
[{{ site.data.cv.email }}](mailto:{{ site.data.cv.email }}){% if site.data.cv.alt_email %} • [{{ site.data.cv.alt_email }}](mailto:{{ site.data.cv.alt_email }}){% endif %} •
[Website]({{ site.data.cv.website }}){% if site.data.cv.linkedin %} • [LinkedIn]({{ site.data.cv.linkedin }}){% endif %}{% if site.data.cv.orcid %} • [ORCID]({{ site.data.cv.orcid }}){% endif %}

---

## Summary
{{ site.data.cv.summary }}

---

## Education
{% for edu in site.data.cv.education %}
- **{{ edu.degree }}**, {{ edu.institution }} — {{ edu.location }} ({{ edu.year }})
  {% if edu.thesis %}<br><em>Thesis:</em> {{ edu.thesis }}{% endif %}
{% endfor %}

{% if site.data.cv.additional_courses_and_workshops %}
<br>
**Additional Courses & Workshops**  
{% for c in site.data.cv.additional_courses_and_workshops %}
- {{ c }}
{% endfor %}
{% endif %}

---

## Experience
{% for role in site.data.cv.experience %}
- **{{ role.title }}**, {{ role.institution }} — {{ role.location }} ({{ role.years }})
  {% if role.lab %}<br><em>{{ role.lab }}</em>{% endif %}
  {% if role.highlights %}
  <ul>
  {% for h in role.highlights %}
    <li>{{ h }}</li>
  {% endfor %}
  </ul>
  {% endif %}
{% endfor %}

---

## Skills
{% for block in site.data.cv.skills %}
- **{{ block.category }}**
  <ul>
  {% for item in block.items %}
    <li>{{ item }}</li>
  {% endfor %}
  </ul>
{% endfor %}

---

## Languages
{% if site.data.cv.languages %}
<ul>
{% for lang in site.data.cv.languages %}
  <li>
    <strong>{{ lang.name }}</strong>
    {% if lang.since %}(since {{ lang.since }}){% endif %}
    {% if lang.focus %} — {{ lang.focus }}{% endif %}
  </li>
{% endfor %}
</ul>
{% endif %}

## Tools & Platforms
{% if site.data.cv.tooling %}
<ul>
{% for tool in site.data.cv.tooling %}
  <li>
    <strong>{{ tool.name }}</strong>
    {% if tool.since %}(since {{ tool.since }}){% endif %}
    {% if tool.focus %} — {{ tool.focus }}{% endif %}
  </li>
{% endfor %}
</ul>
{% endif %}

---

## Accomplishments
{% if site.data.cv.accomplishments %}
<ul>
{% for a in site.data.cv.accomplishments %}
  <li>{{ a | markdownify | remove: '<p>' | remove: '</p>' }}</li>
{% endfor %}
</ul>
{% endif %}

---

## Organizations & Leadership
{% if site.data.cv.organizations %}
<ul>
{% for org in site.data.cv.organizations %}
  <li>
    <strong>{{ org.name }}</strong>{% if org.role %} — {{ org.role }}{% endif %}{% if org.years %} ({{ org.years }}){% endif %}
    {% if org.notes %}
    <ul>
      {% for n in org.notes %}
      <li>{{ n }}</li>
      {% endfor %}
    </ul>
    {% endif %}
  </li>
{% endfor %}
</ul>
{% endif %}

---

## Conferences & Presentations
{% if site.data.cv.conferences_and_presentations %}
<ul>
{% for item in site.data.cv.conferences_and_presentations %}
  <li>{{ item }}</li>
{% endfor %}
</ul>
{% endif %}

---

[View Publications](/publications/)
