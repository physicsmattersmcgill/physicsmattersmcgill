---
layout: page
title: "Activités"
lang: fr
meta_title: ""
subheadline: ""
teaser: ""
header:
   image_fullwidth: "header_unsplash_9.jpg"
permalink: "/activities_fr/"
---
{% for activity in site.activities_fr %}
  <div class="row">
    <div class="small-12 columns b60">

    {% if activity.image.thumb %}<a href="{{ site.url }}{{ site.baseurl }}{{ activity.url }}" title="{{ activity.title_fr }}"><img src="{{ site.urlimg }}{{ activity.image.thumb }}" class="alignleft" width="150" height="150" alt="{{ activity.title_fr }}"></a>{% endif %}

    <h4>{{ activity.title_fr }}</h4> {% if activity.objective_fr %}{{ activity.objective_fr }}{% endif %}
    <a href="{{ site.url }}{{ site.baseurl }}{{ activity.url }}" title="{{ site.data.language.read }} {{ activity.title_fr }}"><strong>{{ site.data.language.read_more }}</strong></a>

    </div>
  </div>
{% endfor %}
