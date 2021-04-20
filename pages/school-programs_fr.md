---
layout: page
title: "Un(e) physicien(ne) dans ta classe!"
lang: fr
meta_title: ""
subheadline: ""
teaser: ""
header:
   image_fullwidth: "20170506_103837_banner.jpg"
permalink: "/school-programs_fr/"
---

Nous organisons des visites ponctuelles ou mensuelles dans les classes. Notre plus récente initiative, le Programme des Explorateurs de l'Espace, propose un panel d'activités couvrant des thèmes de la physique appliqués au contexte de l'exploration spatiale. Ce programme est destinés aux élèves des classes de primaire et est ouvert à tout enseigant des commissions scolaires montréalaises.

**Notez qu’en réponse à la pandémie, nous réalisons maintenant une version virtuelle de notre programme Explorateurs de l’Espace!** Veuillez visitez [ce lien]({{ site.url }}{{ site.baseurl }}/virtual-space-explorers_fr) pour plus d'information.

## Explorateurs de l’espace
<img src="{{ site.urlimg }}SpaceExplorersLogo.png" alt="Logo of McGill Space Explorers program" style="height:200px; float:left; padding-right:10px;">

Nous rendons visite à votre classe par groupe de deux. Le programme comprend cinq visites possiles à répartir au long de l'année selon les disponibilités de chacun. Ces activités sont l'occasion pour les élèves de rencontrer des chercheuses et chercheurs modernes tout en approfondissant les thèmes du programme d'enseignement. Nos activités interactives abordent des thèmes tels que la chaleur et la température, les collisions, la gravité, le magnetisme, la lumière et les couleurs, le fait de flotter ou de couler ainsi que les forces. Le programme est développé de sorte que les élèves sont encouragés à formuler une démarche scientifique complète (hypothèse, modelisation, prise de données et analyse). À la fin du programme, chaque élève reçoit un certificat.
{% for activity in site.activities %}
{% if activity.spaceexplorers %}
- [{{ activity.title_fr }}]({{ site.url }}{{ site.baseurl }}{{ activity.url }}){% endif %}
{% endfor %}

6 écoles sont actuellement partenaires du programme, ce qui représente un bassin d'une centaine d'élèves de la 4ème à la 6ème primaire.

<!--Pour trouver des autres activités et ressources, veuillez visiter le site web de <a href="https://www.mcgill.ca/science/outreach">vulgarisation scientifique</a> de la faculté des sciences !-->
