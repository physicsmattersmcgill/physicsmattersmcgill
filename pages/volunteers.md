---
layout: page
title: "Volunteers"
lang: en
meta_title: ""
subheadline: ""
teaser: ""
header: no
permalink: "/volunteers/"
---
{% for volunteer in site.volunteers %}
{% unless volunteer.lang == "fr" %}
   <div class="row">
   <div class="small-12 columns b60">

   {% if volunteer.image.thumb %}<a href="{{ site.url }}{{ site.baseurl }}{{ volunteer.url }}" title="{{ volunteer.title }}"><img src="{{ site.urlimg }}{{ volunteer.image.thumb }}" class="alignleft" width="150" height="150" alt="{{ volunteer.title }}"></a>{% endif %}

   <h4>{{ volunteer.title }}</h4> {% if volunteer.objective %}{{ volunteer.objective }}{% endif %}
   <a href="{{ site.url }}{{ site.baseurl }}{{ volunteer.url }}" title="{{ site.data.language.read }} {{ volunteer.title }}"><strong>{{ site.data.language.read_more }}</strong></a>

   </div>
   </div>
{% endunless %}
{% endfor %}
