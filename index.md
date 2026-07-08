---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: "APL's site"
---

<h1 style="text-align: center;">Welcome!</h1>

---


## This is a place for my projects, academic and otherwise.

#### Scientifically:

My broad goal is to bring the art of designing metalloenzymes into a predictable engineering discipline. This is to support the development of 1) novel biotechnologies and 2) bio-inspired catalysts. The site is also a space for sharing work from the Cutting Room Floor, which I think is significant enough to release publicly but does not fit neatly into a publication.


#### But also:

This is also a blog to showcase my non-academic projects, along with a collection of my thoughts and other writings.


---

## Recent Posts

{% if site.posts and site.posts.size > 0 %}
<ul>
  {% for post in site.posts limit:3 %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <small>— {{ post.date | date: "%b %d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>

[View all posts](/blog/)
{% else %}
<p>No posts yet.</p>
{% endif %}



