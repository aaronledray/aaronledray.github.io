---
layout: home
title: "Aaron P. Ledray"
description: >-
  I am a metallobiochemist working at the experiment–theory–simulation interface. I study enzyme design, metal-centered reactivity, and research software.
---

# Aaron P. Ledray

I am a postdoctoral researcher in biochemistry at the University of Texas at Austin. My work sits at the intersection of experiment, theory, and simulation, with a focus on designing and understanding metal-containing enzymes.

I am interested in how protein environments control metal-centered reactivity, and how those principles can be used to build useful biotechnologies and bio-inspired catalysts. This site is where I share research, publications, computational tools, works in progress, and writing from the cutting room floor.

## Explore

- [Research and experience]({{ '/about/' | relative_url }})
- [Publications]({{ '/publications/' | relative_url }})
- [Posts]({{ '/blog/' | relative_url }})

## Recent posts

{% if site.posts and site.posts.size > 0 %}
<ul>
  {% for post in site.posts limit:3 %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a><br>
      <small>{{ post.date | date: "%B %-d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>

[View all posts]({{ '/blog/' | relative_url }})
{% else %}
<p>No posts yet.</p>
{% endif %}

## Elsewhere

You can find my formal academic record in the [CV]({{ '/cv/' | relative_url }}) and my research profile on [Google Scholar](https://scholar.google.com/citations?user=zpRylnEAAAAJ&hl=en&oi=ao), [ORCID](https://orcid.org/0000-0002-1829-1235), and [GitHub](https://github.com/aaronledray).
