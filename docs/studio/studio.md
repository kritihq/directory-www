# Kriti Studio

Kriti Studio is a web-only, no code, drag and drop builder which
allow you to design your sites however you see fit. Its your brand after all.

## Prerequisites

1. A directory is already created. [How to?](/docs/new-directory)
2. All the data is ready in `.xlsx` file and imported. [How to?](/docs/data)

## Post import & web pages

After importing data, some web pages are auto generated based on the data. You can view this pages on top left corner drop down menu.

By default `index` and `404` are always present. `index` is the landing page and `404` is error page when visitor tries to access any URL which is not
served by the directory.

Post import, more pages are added based on collections (worksheets) in the `.xlsx` file. For every imported collection 2 pages are added:

1. `/collection`: Home page for that particular collection. E.g. `/jobs` is homepage for jobs collections which will list all the jobs in this excel file.
2. `/collection/{{ record }}`: Page generated for individual row/record/listing in the collection. E.g. individual job listing from jobs.


## Adding elements

Select any page from top left corner and you can start adding elements to it. There are 2 types of elements:

1. Static: Remains constant irrespective of the record.
2. Dynamic: Data changes based on page URL.

### Adding static elements

To begin, start by opening the elements pane from right side and drag any element on to the canvas.

__Demo:__ Adding a H1 (header 1) element

<video controls width="100%">
  <source src="/assets/docs/drag-drop-elems.mp4" type="video/mp4" />
</video>

__Demo 2:__ Adding an IMG (image) element
Certain elements require additional data to be displayed. E.g. Image or Link which require to you add src attributes.

<video controls width="100%">
  <source src="/assets/docs/drag-drop-img.mp4" type="video/mp4" />
</video>

### Adding dynamic elements

Depending on the element, dynamic variables must be added to the element. These variables are available from Data tab on the right section.
These variables are the columns present in respective collections.

_For text types_, edit the text and add text in following format `{{ record "<column name>" }}`.
Here `<column name>` is column name from the spreadsheet.
Or better yet, just copy the column from Data tab.

__Demo__:

<video controls width="100%">
  <source src="/assets/docs/dynamic-text.mp4" type="video/mp4" />
</video>

_For image or link_, Images and link require extra information to work. This fields
are available under Styles tab. Process is still the same, add `{{ record "<column name> }}` or
copy column from Data tab.

__Demo__:

<video controls width="100%">
  <source src="/assets/docs/dynamic-img.mp4" type="video/mp4" />
</video>

## Add Listings

Since this is a directory there will be a need to add list of records (for any collection) somewhere.
There is already an element for that called "listing" in the "Elements" tab, drag and drop it on to canvas on any page.

After dropping it must be configured which is done from "Styles" tab.

<figure>
    <img src="/assets/docs/listings-config.png" alt="Configs for listings element" width="100%">
    <figcaption>Configs for listings element</figcaption>
</figure>

1. Collection: Refers to which collection (worksheet) this listing refers to
2. Page Size: How many records must be fetched in 1 go, listings is an infinite scroll element which fetches records in batches
3. Direction: Ascending or Descending order based on `id` column of the collection

To edit the listings, edit the very first element other elements will mimic it. By default `title` column and the record's `Page URL` are provided.
You can add more elements like image, description etc. to the listing make sure to bind variables from the same collection to them.

_Demo_: Following video demonstrates how to add listing on `/index` page for "companies" collection.

<video controls width="100%">
  <source src="/assets/docs/listings.mp4" type="video/mp4" />
</video>

Any listing to any page i.e. it is possible to add listings for "companies" on "/jobs" page (would not makes sense but possible).
