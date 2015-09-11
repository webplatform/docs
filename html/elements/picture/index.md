---
title: picture
attributions:
  - 'This content was originally published on [DevOpera](http://dev.opera.com), Opera''s Developer Network. .'
code_samples:
  - 'http://googlechrome.github.io/samples/picture-element/'
notes:
  - 'Add Category, Parent,  Children information and HTML information subsection. Complete Compatibility table.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLPictureElement](/dom/HTMLPictureElement)'
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
summary: 'Control which image resource a user agent presents to a user, based on media query and/or support for a particular image format.'
tags:
  - Markup
  - Elements
  - DOM
  - HTML
  - Media
uri: html/elements/picture

---
## <span>Summary</span>

Control which image resource a user agent presents to a user, based on media query and/or support for a particular image format.

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [HTMLPictureElement](/dom/HTMLPictureElement)

The **picture** element (`<picture>`) addresses use cases that are left unaddressed by the srcset attribute, the most important being art direction.

Other use cases, such as matching media features and media types and matching on supported image formats, are also addressed by this element.

### <span>Attributes</span>

This element supports the HTML5 [global attributes](/html/global_attributes).

## <span>Examples</span>

**Art direction use case::** This example shows the basic usage of the picture element for responsive images and art direction.

``` html
<picture>
  <source media="(min-width: 650px)" srcset="images/kitten-large.png">
  <source media="(min-width: 465px)" srcset="images/kitten-medium.png">
  <!-- img tag for browsers that do not support picture element -->
  <img src="images/kitten-small.png" alt="a cute kitten">
</picture>
```

[View live example](http://googlechrome.github.io/samples/picture-element/)

**Different image types use case:** Browsers that support WebP get a WebP image; other browsers get JPG.

``` html
<picture>
  <source
    srcset="opera.webp"
    type="image/webp">
    <img
      src="opera.jpg" alt="The Oslo Opera House">
</picture>
```

**High-DPI images & art direction use case:** For browser windows with a width of 1024 CSS pixels and wider, a full-shot photo is used; smaller browser windows get a close-up photo. In addition, these photos are served as high-resolution images to browsers on devices with high-DPI screens; other browsers get a normal image.

``` html
<picture>
  <source
    media="(min-width: 1024px)"
    srcset="opera-fullshot-1x.jpg 1x, opera-fullshot-2x.jpg 2x, opera-fullshot-3x.jpg 3x">
  <img
    src="opera-closeup-1x.jpg" alt="The Oslo Opera House"
   srcset="opera-closeup-2x.jpg 2x, opera-closeup-3x.jpg 3x">
</picture>
```

**Changing image sizes & art direction use case:** For browser windows with a width of 1280 CSS pixels and wider, a full-shot photo with a width of 50% of the viewport width is used; for browser windows with a width of 640-1279 CSS pixels, a photo with a width of 60% of the viewport width is used; for less wide browser windows, a photo with a width that is equal to the full viewport width is used. In each case, the browser picks the optional image from a selection of images with widths of 200px, 400px, 800px and 1200px, keeping in mind image width and screen DPI.

``` html
<picture>
  <source
    media="(min-width: 1280px)"
    sizes="50vw"
    srcset="opera-fullshot-200.jpg 200w, opera-fullshot-400.jpg 400w, opera-fullshot-800.jpg 800w, opera-fullshot-1200.jpg 1200w">
  <img
    src="opera-fallback.jpg"
    alt="The Oslo Opera House"
    sizes="(min-width: 640px) 60vw, 100vw"
    srcset="opera-closeup-200.jpg 200w, opera-closeup-400.jpg 400w, opera-closeup-800.jpg 800w, opera-closeup-1200.jpg 1200w">
</picture>
```

## <span>Usage</span>

     The picture element is not a general replacement for the img element. When there is only a single image source, authors should use <img> as usual.

The picture element requires `<source>` nested as a child.

The picture element requires `<img>` nested as the last child; without the img element, `<picture>` will be ignored. This requirement ensures maximum accessibility and browser backwards compatibility.

For accessibility, place alternative text for all images in the `alt` attribute of the img element.

## <span>Related specifications</span>

[RICG](http://picture.responsiveimages.org/)
:   Superseded

[WHATWG](http://www.whatwg.org/specs/web-apps/current-work/multipage/embedded-content.html#embedded-content)
:   Living Standard

## <span>See also</span>

### <span>Other articles</span>

-   [\<img\> Element](http://docs.webplatform.org/wiki/html/elements/img)
-   [\<source\> Element](http://docs.webplatform.org/wiki/html/elements/source)

### <span>External resources</span>

-   [Responsive Images: Use Cases and Documented Code Snippets to Get You Started](http://dev.opera.com/articles/responsive-images/)
