---
layout: page
title: "Volunteers"
lang: fr
meta_title: ""
subheadline: ""
teaser: ""
header: no
permalink: "/volunteers_fr/"
---
{% for volunteer in site.volunteers_fr %}
{% unless volunteer.lang == "fr" %}
   <div class="row">
   <div class="small-12 columns b60">

   {% if volunteer.image.thumb %}<a href="{{ site.url }}{{ site.baseurl }}{{ volunteer.url }}" title="{{ volunteer.title_fr }}"><img src="{{ site.urlimg }}{{ volunteer.image.thumb }}" class="alignleft" width="150" height="150" alt="{{ volunteer.title_fr }}"></a>{% endif %}

   <h4>{{ volunteer.title_fr }}</h4> {% if volunteer.objective_fr %}{{ volunteer.objective_fr }}{% endif %}
   <a href="{{ site.url }}{{ site.baseurl }}{{ volunteer.url }}" title="{{ site.data.language_fr.read }} {{ volunteer.title_fr }}"><strong>{{ site.data.language_fr.read_more }}</strong></a>

   </div>
   </div>
{% endunless %}
{% endfor %}
