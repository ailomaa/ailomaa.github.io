# gu-clasp.github.io README

## About this site

This site is built with [jekyll](https://github.com/jekyll/jekyll), a static web site generator framework for Ruby. [Github Pages](https://pages.github.com/) has builtin support for this.

## Site configuration

Configuration for the site is done from `_config.yml'.

...

## Adding content to this site

Content is always added under `./src/`. Any markdown or html files added here will be built into static html files that are served from `./public/`.

### About collections

Jekyll has support for something called [collections](https://jekyllrb.com/docs/collections/). Any non-standard directory name beginning with an underscore, such as `_events` will be interpreted as a collection. Collections can be iterated using liquid.

Adding to collections means adding at least a directory containing an `index.md`.

Example contents for an event:
```(text)
./src/_events/2024-12-24-christmas-eve/
./src/_events/2024-12-24-christmas-eve/index.md
./src/_events/2024-12-24-christmas-eve/santa.jpg
./src/_events/2024-12-24-christmas-eve/slides.pdf
./src/_events/2024-12-24-christmas-eve/schedule.pdf
```

#### Adding events

Use the [event template]() to create your event under `./src/_events`.

Edit the metadata in `index.md`, so that the event will be displayed correctly. ***Take special care with the date format***.

The metadata will be displayed at the top of the event page on the site. Remove any metadata that does not apply to the event.

Any text below the metadata will be intepreted as markdown.

```(liquid)
---
title: Christmas Eve
presenters: Santa Claus and his helpers
date: 2024-12-24 15:00
location: Short description
---

This text is interpreted as markdown and translated to html.

* List item 1
* List item 2

Showing an [Example Link](https://url-to-somewhere)

Including downloadable files that are placed in the same directory with this file.

![Timetable](./timetable.pdf)

The same syntax for displaying an image
![Image](./image.jpg)

```


#### Adding people
