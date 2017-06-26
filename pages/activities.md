---
layout: page
title: "Activities"
lang: en
meta_title: ""
subheadline: ""
teaser: ""
header:
   image_fullwidth: "header_unsplash_9.jpg"
permalink: "/activities/"
---
{% for activity in site.activities %}
  <div class="row">
    <div class="small-12 columns b60">

    {% if activity.image.thumb %}<a href="{{ site.url }}{{ site.baseurl }}{{ activity.url }}" title="{{ activity.title }}"><img src="{{ site.urlimg }}{{ activity.image.thumb }}" class="alignleft" width="150" height="150" alt="{{ activity.title }}"></a>{% endif %}

    <h4>{{ activity.title }}</h4> {% if activity.objective %}{{ activity.objective }}{% endif %}
    <a href="{{ site.url }}{{ site.baseurl }}{{ activity.url }}" title="{{ site.data.language.read }} {{ activity.title }}"><strong>{{ site.data.language.read_more }}</strong></a>

    </div>
  </div>
{% endfor %}
