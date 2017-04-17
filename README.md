This is the repository for the Physics Matters McGill website, https://physicsmattersmcgill.github.io/physicsmattersmcgill/lectures/

# Adding a page or changing the navigation menu
The data for the navigation menu (page names, what goes in each menu) goes in the folder `_data/navigation.yml`.

To make a new page, add a new markdown file under the `pages/` folder. See existing pages for examples and the front matter to use.

# Images  
Any images used on the site should be in the images folder.

Images to be used as thumbnails should be sized to be 150x150 pixels.

# Adding an event
- Add a new file to the `_events` folder.
  - For a public lecture the name of the event should have the format `lecture-YYYY-MM-DD-anytext`.
  - In the front-matter, include the following fields:
```  ---
  layout: event
  title: "Any title - in quotes"
  speaker: "Speaker Name (Affiliation of Speaker)"
  #speaker_url: "website in quotes" #delete this line if no website
  event-date: YYYY-MM-DD HH:MM  #date of the event
  location: "the Keys Auditorium (Rutherford Physics Building, room 112), McGill University"  #this will probably be the same for all lectures
  image:
      title: filename_of_title_image #This image goes at the top of the page
      thumb: filename_of_thumbnail #This should be a 150x150 px thumbnail
  type: lecture   #if this is lecture, then the event will show up on the public lecture page, otherwise it will not show up on the public lecture page
  tags:   # Add tags as a list (with dashes). For example:
    - medical physics
    - cancer
    - radiation
  #
  # Styling
  #
  header: no
  mediaplayer: false
  ---
