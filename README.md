This is the repository for the Physics Matters McGill website, https://physicsmattersmcgill.github.io/physicsmattersmcgill

This README is meant to help someone to update the Physics Matters website. This website was built using the [Feeling Responsive template](http://phlow.github.io/feeling-responsive/).

# Adding a page or changing the navigation menu
The data for the navigation menu (page names, what goes in each menu) goes in the folder `_data/navigation.yml`.

To make a new page, add a new markdown file under the `pages/` folder. See existing pages for examples and the front matter to use.

# Images  
Any images used on the site should be in the images folder.

Images to be used as thumbnails should be sized to be 150x150 pixels and start with `thumb_`.

# Adding an event
New events are added as elements of a jekyll collection - this is called the events collection. Each event has its own markdown file (extension: `.md`) in the `_events` folder which marks it as part of the collection.

## Naming convention for the markdown files
For a Physics Matters public lecture, start the event with `lecture-`. For all events, please include the date as part of the name of the file using the format `YYYY-MM-DD`.  For example, this might be the filename for a public lecture: `lecture-YYYY-MM-DD-shorttopicname.md`. Note that the McPherson lecturs should not be in this category, since they are another program, and have their own page.

Each of the events has frontmatter which will help define it as an event and make sure the style and formatting is consistent on the website. The frontmatter is in between the three dashes (`---` both above and below). Here is the frontmatter for an event (comments after `#` are ignored by jekyll and are there to explain the field)
```
  layout: event
  title: Event Title
  meta_description: Short description that goes on the event listing page. Note: Do NOT use the full abstract - it is too long! Break up the title if it's long and/or use 1-2 sentences from the abstract.
  speaker: Speaker Name (Affiliation of Speaker)
  speaker_url: website_URL #delete this line if no website
  event-date: YYYY-MM-DD HH:MM  #date of the event - the format is important!
  location: the Keys Auditorium (Rutherford Physics Building, room 112), McGill University  #this will probably be the same for all lectures
  image:
  image:
      title: lecture_hall_empty.jpg #Use this as default if no image is given
      thumb: thumb_lecture_hall_empty.jpg #Use this as default if no image is given
      caption: Image from ... #If there's an image credit, add it here. If not, delete this line
  type: lecture   #if this is lecture, then the event will show up on the public lecture page, otherwise it will only show up on the event page
  tags:   # Add tags as a list, for example,
    - particle physics
    - biophysics
    - climate
    - nanotechnology
    - etc.
  #
  # Styling
  #
  header: no   #turns off the header image (the title image is placed at the top of the page instead of a header)
  mediaplayer: false
  ```
  Finally, add a description of the event in the markdown file. Feel free to use any markdown styling (see examples.)

# Adding new Partners
The partners.md file contains links to partners. These should be added as a list in the frontmatter. Each partner must include a link, and may include either a logo or text. It could also include both (useful in cases where the logo doesn't include the name of the group/partner.) Each new partner gets a new `-` in the `links` list. For example,
```
links:
  - url: http://www.astro.physics.mcgill.ca/outreach.php
    logo: partnerlogo_AstroMcGill.png
```
