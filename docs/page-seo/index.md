# Page Metadata & SEO

This documentation explains how to add page meta data in your application using the built-in "Page Meta & SEO" panel. The panel provides an easy way to manage meta data fields to improve your page’s SEO. Follow the instructions below to add new meta data fields and input the necessary information.

<video controls width="100%">
  <source src="/assets/docs/page-seo/seo-demo.webm" type="video/webm" />
</video>

## Adding Metadata

1. __Accessing the "Page Meta & SEO" Panel__

  Locate and click the accordian "Page Meta & SEO" on top left corner below page selector. Clicking on it will expand the section to reveal the meta data form.

  ![Page Meta & SEO Panel](/assets/docs/page-seo/seo-locate-panel.gif)

<br/>

2. __Adding a New Field__

  Find the "Add" drop down at bottom of the Page Meta & SEO panel. It has some preconfigured `<meta />` fields along with "Custom" option.
  Preconfigured `<meta />` fields add known meta tags like `title`, `description`, `keywords`, etc to page. If any field is not listed, use the "Custom" option to add a new field.

  <img src="/assets/docs/page-seo/seo-add.png" alt="Add Meta Field"  style="width: 400px; height: 400px;">

  It makes sense for certain fields to be duplicated for same page e.g. `Favicon` but not others e.g. `Title`, `Description` or `Canonical URL`.

<br/>

3. __Entering Values into the New Field__

  Every meta item has one or more input field corresponding to an attribute of `<meta />` tag. Enter the appropriate values for the field. Make sure the values meet any specific requirements or character limits defined by your overall SEO strategy.

  ![Meta Field Static values](/assets/docs/page-seo/seo-static-values.webp)

  These input fields support both static and dynamic values. For dynamic values, use the `{{ }}` syntax to reference a variable or a function.
  For pages such as `index` or `404` page may require static values since they stay constant but for dynamic pages generated for every collection, it makes more sense to have dynamic values. Use the data panel from right hand side to easily copy a data variable.

  ![Meta Field Dynamic values](/assets/docs/page-seo/seo-dynamic-values.webp)

<br/>

4. __Custom Meta fields__

  To add custom `<meta />` fields, select the "Custom" option from the "Add" dropdown. This will add a new field to the form where you can enter the name of the meta tag and its content. This field also support static and dynamic values.

  ![Meta Custom Field Static value](/assets/docs/page-seo/seo-custom-static.webp)

  For dynamic values,

    - it is possible to add these values for attributes such as
      ![Meta Custom Field Dynamic attributes](/assets/docs/page-seo/seo-custom-dynamic-1.webp)
    - or add complete `<meta />` tag as dynamic value.
      ![Meta Custom Field Dynamic value](/assets/docs/page-seo/seo-custom-dynamic-2.webp)

<br/>

5. __Ordering Meta Fields__

  Certain meta tags such as stylesheets, scripts, etc. need to be ordered in a specific way. To reorder the meta fields, click the arrow buttons on left side of the field to move it up or down in the list. This provides precise control over the order of the meta tags and ensures that they are rendered correctly in the page’s HTML.

  Note: The order of meta tags can affect the page’s performance and SEO, so it is important to arrange them properly. This can also affect page is rendered when custom stylesheets are provided.

<br/>

6. __Removing a Field__

  Click the cross button on right side of the field to remove it from the list. This will delete the field and its content from the page’s meta data.
