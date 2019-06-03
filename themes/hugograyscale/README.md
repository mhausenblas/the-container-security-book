# Grayscale Theme for Hugo
This is a multi-section single page theme intended as a landing page.  This is derived from the startbootstrap-grayscale theme.

Preview at https://runningstream.github.io/hugograyscale/

## Configuration
The Hugo Grayscale theme is a one page theme designed to be the front page to your site.  Its content is populated via the front-matter in `content/_index.md`.  The page consists of, in order:
* a navbar at top linking to the other sections, and other arbitrary links
* an intro section presenting a header title and into text with background image
* an about section presenting a header and text with black background
* a download section presenting header and text with background image
* a contact section presenting header and text with black background
 
The section names show up as the links in the navbar, so you may wish to rename them if, for example, you're not using it for the purpose suggested by the default section name.
 
The background images are selected by filename - the intro section image must be named "intro-bg.jpg" and placed in the "static/img/" directory for your site.  Similarly, the downloads section image must be named "downloads-bg.jpg" and placed in the "static/img/" directory for your site.  See the default images in the theme's static directory for file size reference.

Check out the exampleSite `content/_index.md` for a full-featured example, or look below...

```YAML
---
title: "Hugo Grayscale Theme"
date: 2018-09-09T00:00:00-00:00
copyright: "Your Website"
#mapsapikey: xxx

socialhandles:
    twitter: "stream_running"
    github: "runningstream"
#    googplus: "goog_addr_here"

menu:
    -
        url: "http://startbootstrap.com/template-overviews/grayscale/"
        name: "Original"

intro:
    header: "Grayscale"
    text: "A free, responsive, one page Hugo/Bootstrap theme originally created by Start Bootstrap."

about:
    header: "About Grayscale"
    text: '<p>Grayscale is a free Bootstrap theme created by Start Bootstrap. It can be yours right now, simply download the template on <a href="http://startbootstrap.com/template-overviews/grayscale/">the preview page</a>. The theme is open source, and you can use it for any purpose, personal or commercial.</p> <p>This theme was also adapted from a Jekyll version, brought to you by <a href="https://github.com/jeromelachaud">Jerome Lachaud</a></p> <p>This theme features stock photos by <a href="http://gratisography.com/">Gratisography</a> along with a custom Google Maps skin courtesy of <a href="http://snazzymaps.com/">Snazzy Maps</a>.</p> <p>Grayscale includes full HTML, CSS, and custom JavaScript files along with SASS and LESS files for easy customization!</p>'

download:
    rename: "Links"
    header: "Download Grayscale"
    text: '<p>You can download Grayscale for free on the preview page at Start Bootstrap.</p><a href="http://startbootstrap.com/template-overviews/grayscale/" class="btn btn-default btn-lg">Visit Download Page</a>'

contact:
    header: "Contact Start Bootstrap"
    text: '<p>Feel free to leave us a comment on the <a href="http://startbootstrap.com/template-overviews/grayscale/">Grayscale template overview page</a> on Start Bootstrap to give some feedback about this theme!</p>'
---
```

## Usage
Drop it in your site's themes folder, then modify your site config file to specify the theme `grayscale`, or use the `-t grayscale` command line switch.
