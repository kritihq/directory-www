# Kriti Studio

Kriti Studio is a web-only, no code, drag and drop builder which
allow you to design your sites however you see fit. Its your brand after all.

## Prerequisites

1. A directory is already created. [How to?](/docs/new-directory)
2. All the data is ready in `.xlsx` file and imported. [How to?](/docs/data)


## How to design

To begin, start by opening the elements pane from right side and drag any element on to the canvas.

__Demo:__ Adding a H1 (header 1) element

<video controls width="100%">
  <source src="/assets/docs/drag-drop-elems.mp4" type="video/mp4" />
</video>

__Demo 2:__ Adding an IMG (image) element
Certain elments require additional data to be displayed. E.g. Image or Link which require to you add src attributes.

<video controls width="100%">
  <source src="/assets/docs/drag-drop-img.mp4" type="video/mp4" />
</video>


## Element types: static vs dynamic

Content can be either of
1. Static: Always constant no matter what, imagine static text on webpage.
2. Dynamic: Depends on webpage's slug, imagine text or an image which changes based on each record's page.

### Adding static elements

Its rather easy just drag and drop any element on to canvas. Its static by default.

### Adding dynamic elements

Drag any element onto canvas. Depending on element type you'll have to add dynamic content.

__For text types__, edit the text and add text in following format `{{ record "<column name>" }}`.
Here `<column name>` is column name from the spreadhseet.
Or better yet, just copy the column from Data tab.

Demo:

<video controls width="100%">
  <source src="/assets/docs/dynamic-text.mp4" type="video/mp4" />
</video>

__For image or link__, Images and link require extra information to work. This fields
are available under Styles tab. Process is still the same, add `{{ record "<column name> }}` or
copy column from Data tab.

Demo:

<video controls width="100%">
  <source src="/assets/docs/dynamic-img.mp4" type="video/mp4" />
</video>
