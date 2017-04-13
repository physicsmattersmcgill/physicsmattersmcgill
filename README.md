This is the repository for the Physics Matters McGill website, https://physicsmattersmcgill.github.io/physicsmattersmcgill/lectures/

# Images  
Any images used on the site should be in the images folder.

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
      title: image title #can be the filename
      thumb: filename_of_image
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
