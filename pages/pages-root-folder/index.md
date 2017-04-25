---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: frontpage
header:
  image_fullwidth: collisions_top_kids.jpg
  caption: "Image credit: Gabriel Kocher (2015)"
widget1:
  title: "Public Lectures"
  url: "{{ site.baseurl }}/lectures/"
  image: public_lecture.jpg
  text: 'Join us for cutting edge science! These lectures are aimed at anyone who wants to learn more about current physics topics - no science background is necessary. Whether you are a long-time science enthusiast, or have developed a new interest in physics, we invite you to join us to learn about cutting edge science from the experts doing the research!'
widget2:
  title: "Space Explorers"
  url: "/space-explorers/"
  image: collisions_top_kids.jpg
  text: 'The Space Explorers program is a way for kids to explore physics in fun, self-contained, and hands-on modules. Pairs of volunteers visit local classrooms around 5 times over the course of a school year, giving primary school kids a chance to get to know a physicist, while doing educational activities.'
widget3:
  title: "And much more!"
  url: "{{ site.baseurl }}"
  image: widget-github-303x182.jpg
  text: 'blah blah blah'
#
# Use the call for action to show a button on the frontpage
#
# To make internal links, just use a permalink like this
# url: /getting-started/
#
# To style the button in different colors, use no value
# to use the main color or success, alert or secondary.
# To change colors see sass/_01_settings_colors.scss
#
#callforaction:
#  url: https://tinyletter.com/feeling-responsive
#  text: Inform me about new updates and features ›
#  style: alert
permalink: /index.html
#
# This is a nasty hack to make the navigation highlight
# this page as active in the topbar navigation
#
homepage: true
---

<div id="videoModal" class="reveal-modal large" data-reveal="">
  <div class="flex-video widescreen vimeo" style="display: block;">
    <iframe width="1280" height="720" src="https://www.youtube.com/embed/3b5zCFSmVvU" frameborder="0" allowfullscreen></iframe>
  </div>
  <a class="close-reveal-modal">&#215;</a>
</div>
