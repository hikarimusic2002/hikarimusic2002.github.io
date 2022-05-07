---
permalink: /
title: "About"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

* やりたいこと多すぎて結局何もやりきれなかったダメ人間
* CKCOS / IPHO silv. / IBO repr.
* National Taiwan University College of Medicine

Solutions
------

### Physics

  * [Mathematical Methods for Physicists](https://hikarimusic2002.github.io/solutions)

### Mathematics

  * [Principles of Mathematical Analysis](https://hikarimusic2002.github.io/solutions)

### Algorithm

  *  [Codeforces](https://hikarimusic2002.github.io/solutions)



{% capture written_label %}'None'{% endcapture %}

{% for collection in site.collections %}
{% unless collection.output == false or collection.label == "posts" %}
  {% capture label %}{{ collection.label }}{% endcapture %}
  {% if label != written_label %}
  <h2>{{ label }}</h2>
  {% capture written_label %}{{ label }}{% endcapture %}
  {% endif %}
{% endunless %}
{% for post in collection.docs %}
  {% unless collection.output == false or collection.label == "posts" %}
  {% include archive-single.html %}
  {% endunless %}
{% endfor %}
{% endfor %}
