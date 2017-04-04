---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: frontpage
header:
  image_fullwidth: collisions_top_kids.jpg
widget1:
  title: "Public Lectures"
  url: "{{ site.baseurl }}/lectures/"
  image: public_lecture.jpg
  text: 'Join us for cutting edge science! At 7pm on (usually) the first Thursday of each month, the Physics Matters Outreach group hosts lectures about exciting new developments in physics. This event is free of charge and no registration is required. Seats are assigned on a first come first come basis.'
widget2:
  title: "Space Explorers"
  url: "{{ site.baseurl }}/space-explorers/"
  image: collisions_top_kids.jpg
  text: 'The Space Explorers program is a way for kids to explore 5 physics concepts in fun, self-contained, and hands-on modules.'
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
