---
layout: page
title: "Contact Information"
description: >-
  Contact information and professional links for Aaron P. Ledray.
permalink: /contact/
---

# Contact Information

## Let’s Talk!

<!-- Obfuscated emails -->
<p>Email: <span id="email1"></span></p>
<p>UT Email: <span id="email2"></span></p>


## Elsewhere


[Website]({{ site.data.cv.website }})<br>
[LinkedIn]({{ site.data.cv.linkedin }})<br>
[Google Scholar]({{ site.data.cv.scholar }})<br>
[ORCID](https://orcid.org/{{ site.data.cv.orcid }})<br>
[GitHub]({{ site.data.cv.github }})

You can also find me at UT Austin in the [Lu Lab](https://cm.utexas.edu/faculty/yi-lu).

<script>
  // Simple obfuscation for emails
  const e1 = ['aaronledray','gmail.com'].join('@');
  const e2 = ['aledray','utexas.edu'].join('@');
  document.getElementById('email1').textContent = e1;
  document.getElementById('email2').textContent = e2;
</script>
