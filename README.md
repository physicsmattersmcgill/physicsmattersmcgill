This is the repository for the Physics Matters McGill website, https://physicsmattersmcgill.github.io/physicsmattersmcgill

This README is meant to help someone to update the Physics Matters website. This website was built using the [Feeling Responsive template](http://phlow.github.io/feeling-responsive/). Please refer to the template documentation for more details about the template. The information below is specific to our website, and covers all the basic tasks that will be necessary for updating and maintaining this website.

# Are you a Physics Matters volunteer here to help?

Check out the issues list on github!

If you're bilingual, look for the label "translation needed" in light green. Ask questions in the thread if you need help finding a file, or have any questions about the translation.

# Adding a page or changing the navigation menu
The data for the navigation menu (page names, what goes in each menu) goes in the folder `_data/navigation.yml`.

To make a new page, add a new markdown file under the `pages/` folder. See existing pages for examples and the front matter to use.

Each page in the menu must have an English and French title and url in the `_data/navigation.yml` file in order for the menus to work for both English and French versions of the site. The urls provided in this file should match the permalinks in the frontmatter of the corresponding pages. The filenames can be whatever you wish (but it may be easiest if they match the permalink convention). With the exception of the homepage and events pages (which are treated differently) the French version of the page must have a url that is the same as the English version plus `_fr`. For example, `/about/` for the English version and `/about_fr/` for the French version. If there is not going to be a French version of a page, please add the equivalent file anyway (or else the language switcher on the top right of the page will give an error), and this page can have a message (e.g. "Cette page n'est pas disponsible en français.") and either the text of or a link back to the English version.

# Images  
Any images used on the site should be added to the `/WWW/outreach/images` folder on the `elwing` physics department server. Please do NOT put pictures for the website on github. If you need access to this server, please contact [outreach@physics.mcgill.ca](outreach@physics.mcgill.ca). 

Before uploading the image, take a look at its size. It may be necessary to scale down the size for the website. Although this reduces the quality, it will help the page load faster. Typical dimensions will most likely be in the range of 600-1200 pixels, depending on how large it'll be shown on the page.

## Thumbnails
Images to be used as thumbnails should be sized to be 150x150 pixels. Try to make the image as square as possible so that the thumbnails will look consistent when content is listed on a page. If you really need a rectangular image, then set the width to 150 pixels, and the height can be a little flexible.

It is convenient if the filename for thumbnail images starts or ends with `thumb` so that it is easy to tell which are small thumbnail images and therefore should not be used for larger slots on the website

# Videos
First, ask the outreach coordinator to upload the video to the outreach youtube account (associated with the gmail account, physicsmattersmcgill@gmail.com). Then, add the following code in the markdown or html file, replacing the link after `src:` with the link of the youtube video:
`<iframe width="560" height="315" src="https://www.youtube.com/embed/zLNch2v5twc" frameborder="0" allowfullscreen></iframe> `

# Adding an event
New events are added as elements of a jekyll collection - this is called the events collection. Each event has its own markdown file (extension: `.md`) in the `_events` folder which marks it as part of the collection. There is a template you can use the the `_drafts` folder.

## Naming convention for the event files
To help things stay organized: for all events that are NOT physics matters public lectures, please include the date as first part of the file name using the format `YYYY-MM-DD`.

For a Physics Matters public lecture, start the event with `lecture-`. For example, this might be the filename for a public lecture: `lecture-YYYY-MM-DD-shorttopicname.md`. Note that the McPherson lectures should not be in this category, since they are another program, and have their own page. Note that the event type in a Physics Matters public lecture markdown file must be 'lecture' to for the website code to correctly classify the event as "upcoming" or "past."

Each of the events has frontmatter which will help define it as an event and make sure the style and formatting is consistent on the website. The frontmatter is in between the three dashes (`---` both above and below). Here is the frontmatter for an event (comments after `#` are ignored by jekyll and are there to explain the field). You can copy this or the markdown of another event to use as a template.
```
---
title: "Title in English"
title_fr: "Title in French (OPTIONAL - delete if no title)"
meta_description: "Short description that goes on the event listing page. Note: Do NOT use the full abstract - it is too long! Break up the title if it's long and/or use 1-2 sentences from the abstract."
meta_description_fr: "French version of the meta_description"
speaker: "Name of Speaker (affiliation of the speaker)"
speaker_fr: (OPTIONAL - delete if same in French and English)
speaker_url: (OPTIONAL - delete if no url)
event-date: YYYY-MM-DD HH:MM # date and time the event starts- the format is important!
image:
    title: lecture_hall_empty.jpg
    thumb: thumb_lecture_hall_empty.jpg
tags:
  - nonlinear physics
  - solid state physics
  - etc.
  - These are optional
bilingual: true/false #OPTIONAL - if a French title exists, then the page will be bilingual. If there is no alternative title in French, then this defaults to false and a message shows up to say that the page is not available in French. Set to true only to override this behavior (no alternative title in French, but you don't want the message to show up to say the page is not available in French.)
type: lecture
---
Put any other formatting here, like a copy of the talk content description (abstract) in English or French
```
Finally, add a description of the event in the markdown file below the frontmatter. Feel free to use any markdown styling (see examples.) This may be an abstract, or two bilingual descriptions of an event.

# Activities
The activities page will display a list of all of our activities that are available for the public to view/download. These should only be activities that are fully developed - not works in progress.

The activities is a jekyll collection, similar to the events collection. Therefore it does not behave in the same way as regular pages, in particular you do not need to create two files for English and French versions - all the information is contained in one file.

## Adding an activity
Convert any guides/worksheets or other downloadables into pdf format and add these `downloads` folder. When making these, please make sure they are written in a way that is useful for a teacher or other educator. For example: modules for which we constructed something, like the collisions or circuits modules, should have construction information in an appendix. If possible, include alternative materials for anything that might be expensive or hard to get (e.g. metal and plastic spoons instead of square plates of aluminum, copper, and PVC in the heat and temperature module.) It is highly recommended, but not necessary, to have downloadables; for example, some short demonstrations may not have any information to provide besides what is contained in the objective and summary.

Find a nice image to display on the top of the activity page. Ideally, this would show some participants doing the activity, but it could also be an image of some of the equipment. Make a smaller thumbnail version of this image or use another image - the thumbnail should be 150 pixels by 150 pixels. If this is not possible due to the desired aspect ratio of the thumbnail, the image must be 150 pixels wide. Add both of these images to the location where the images are hosted (see the section of this readme on images - the images are NOT hosted on github).

Make a new file in the `_activities` folder and add the English and French frontmatter (see template in `_drafts` folder.) Unlike for the regular pages, you do NOT make two versions for French and English - all the information is contained in one file. Do not add any content after the frontmatter - it will not be shown. The downloads you added to the `downloads` folder should be listed in the frontmatter.

(Note: Do NOT make an activity in the `_activities_fr` folder - this is purely a symbolic link to the `_activities` folder which is needed for the website to build properly. All French information is contained in the same file for the activities collection to allow the activity pages to be bilingual.)

# Adding new Partners
The partners.md file contains links to partners. These should be added as a list in the frontmatter. Each partner must include a link, and may include either a logo or text. It could also include both (useful in cases where the logo doesn't include the name of the group/partner.) Each new partner gets a new `-` in the `links` list. For example,
```
links:
  - url: http://www.astro.physics.mcgill.ca/outreach.php
    logo: partnerlogo_AstroMcGill.png
```

# Languages and translations
For any translated page (*except* homepage and events), the permalink variable in the frontmatter for the translation must be the same as the permalink for the English version with `_fr` at the end. As long as this rule is followed, the language switcher links on the top right of the page will work even as new pages are added.

Translations for website components like buttons and `more` links are contained in `_data/language.yml` for English and `_data/language_fr.yml` for French. The file `_data/languages.yml` contains other language information, such as the language codes and which is the default.

The text for the sidebar on the lectures page is in the file `_includes/_sidebar.html` and for the footer is in `_includes/_footer.html`. There is an if/else loop in each of these files which checks the language. Both languages are in the same file.

Events only have one file. If the event has a French version of the title or other metadata, these can be added to the frontmatter of the event file and will be used on the appropriate page. The same main content is shown on both English and French versions of the pages pages.

# Testing a local copy of the website
You can test the site locally by running
```
$ jekyll serve
```
This will still look for the images at the specified location on the department server as defined in `_config.yml`. If you want to temporarily use a local images folder, you can temporarily use a different configuration file:
```
$ jekyll serve --config _config_dev.yml
```
This configuration file uses a local folder to look for images. You may need to grab all the images from the department server in order to fully test the website locally.

# Deployment

The website is deployed automatically using Travis Continuous Integration (Travis CI for short). So in short, **you do not need to do anything in order for the website to deploy** -- whenever the github repository is updated, the website is automatically rebuilt.

To make any changes to the deployment process, the webmaster should make an account at https://travis-ci.org/. Physics Matters will show up as one of the organizations associated with the webmaster's account. It is currently set up to build the website whenever there is an update, or once a day if there are no updates. The daily builds will ensure that the activity list is always up to date (for example, an event that just occurred will be automatically moved from upcoming to past events.) In addition to this, whenever there's a new pull request, Travis CI will attempt to build the new branch (without merging them into the main project) and will show if there are any errors or if the build occurs without any problems. These checks may take 5-10 min.

How it works: Travis CI will build the website and put the built website on the gh-pages branch. The gh-pages branch should therefore NOT be used by the human developers. Note: from what I understand, the commit history on the gh-pages branch is rewritten by Travis CI.
