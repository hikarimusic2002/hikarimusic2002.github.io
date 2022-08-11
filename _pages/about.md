---
permalink: /
title: "About"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

* National Taiwan University College of Medicine
* 2019 IPHO Participant (Silver)

Solutions
------

Physics

  * [Mathematical Methods for Physicists](https://hikarimusic.github.io/solutions)

Mathematics

  * [Principles of Mathematical Analysis](https://hikarimusic.github.io/solutions)

Algorithm

  *  [Codeforces](https://hikarimusic.github.io/solutions)



{% capture written_label %}'None'{% endcapture %}

{% for collection in site.collections reversed %}
{% unless collection.output == false or collection.label == "posts" %}
  {% capture label %}{{ collection.label }}{% endcapture %}
  {% if label != written_label %}
  <h2>{{ label }}</h2>
  {% capture written_label %}{{ label }}{% endcapture %}
  {% endif %}
{% endunless %}
{% for post in collection.docs reversed %}
  {% unless collection.output == false or collection.label == "posts" %}
  {% include archive-single.html %}
  {% endunless %}
{% endfor %}
{% endfor %}
