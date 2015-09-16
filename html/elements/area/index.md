---
title: 'area'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/imagemap.htm'
compatibility:
  feature: area
  topic: html
notes:
  - 'Add more information in Summary, Notes and Compatibility sections.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLAreaElement](/dom/HTMLAreaElement)'
readiness: 'In Progress'
summary: 'Represents either a hyperlink with some text and a corresponding area on an image map, or a dead area on an image map.'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/area

---
## Summary

Represents either a hyperlink with some text and a corresponding area on an image map, or a dead area on an image map.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLAreaElement](/dom/HTMLAreaElement)

## HTML Attributes

 Global attributes: accesskey, class, contenteditable, dir, hidden, id, lang, spellcheck, style, tabindex, title, translate
:   See [global attributes](/html/global_attributes).
 `alt` = fallback content for the image map
:   If the area element has a href attribute, the alt attribute must be present.
    The alt attribute may be left blank if there is another area element in the same image map that points to the same resource and has a non-blank alt attribute.
 `coords` = valid list of integers
:   This attribute gives the coordinates for the shape described by the shape attribute. The processing for this attribute is described as part of the image map processing model.
    -   In the circle state
        The area elements must have a coords attribute present, with three integers, the last of which must be non-negative.
        -   distance in CSS pixels from the left edge of the image to the center of the circle
        -   distance in CSS pixels from the top edge of the image to the center of the circle
        -   radius of the circle
    -   In the polygon state
        The area elements must have a coords attribute with at least six integers, and the number of integers must be even. Each pair of integers must represent a coordinate given as the distances from the left and the top of the image in CSS pixels respectively, and all the coordinates together must represent the points of the polygon, in order.
    -   In the rectangle state
        The area elements must have a coords attribute with exactly four integers. the first of which must be less than the third, and the second of which must be less than the fourth.
        -   distance from the left edge of the image to the left side of the rectangle
        -   distance from the top edge to the top side
        -   distance from the left edge to the right side
        -   distance from the top edge to the bottom side

`shape` = "circle" / "poly" / "rect" / "default"
:   -   `circle`: Circle keyword represents circle state.
    -   `poly`: Poly keyword represents polygon state.
    -   `rect`: Rect keyword represents rectangle state.
    -   `default`: The area is the whole image. area elements must not have a coords attribute.

 `href` = URL potentially surrounded by spaces
:   A URL that provides the destination of the hyperlink. If the href attribute is not specified, the element represents a placeholder hyperlink.
 `target` = browsing-context name or keyword
:   A name or keyword giving a browsing context for UAs to use when following the hyperlink.
    The target attribute on the a element was deprecated in a previous version of HTML, but is no longer deprecated, as it is useful in Web applications, particularly in combination with the iframe element.
    Any string that is either of the following:
    -   a browsing-context name
    -   any case-insensitive match for one of the following literal strings: "\_blank", "\_self", "\_parent", or "\_top".

 `rel` = set of space-separated tokens
:   A list of tokens that specify the relationship between the document containing the hyperlink and the destination indicated by the hyperlink.
 `hreflang` = language tag
:   The language of the destination of the hyperlink.
    A valid language tag, as defined in [BCP47].
 `media` = media-query list
:   The media for which the destination of the hyperlink was designed.
    A valid media query list, as defined in [MediaQueries].
 `type` = MIME type
:   The MIME type of the destination of the hyperlink.
    A string that identifies a valid MIME media type, as defined in [RFC2046].

## Examples

The following example uses the **area** element inside a parent **map** element to create an image map of the solar system. Each **area** element defines and provides a link to an image on the **map** using the [**coords**](/html/attributes/coords) and [**shape**](/html/attributes/shape) attributes to specify its dimensions and shape, respectively; and the [**title**](/html/attributes/title) attribute to provide a descriptive pop-up tooltip when pointed to with the mouse. A tooltip is especially useful if the image file is missing or cannot be displayed for whatever reason.

``` html
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"
  "http://www.w3.org/TR/html4/loose.dtd">
<html>
<head>
 <meta http-equiv="X-UA-Compatible" content="IE=8"/>
  <title>Image Map Example</title>
  <base href="http://samples.msdn.microsoft.com"/>
</head>
<body>
<p><img src="/workshop/graphics/solarsys.png" width=504 height=126 border=0
    title="Solar System" usemap="#SystemMap"/></p>
  <map name="SystemMap">
      <area shape="rect" coords="0,0,82,126"
        href="/workshop/graphics/sun.png" title="Sun"/>
      <area shape="circle" coords="90,58,3"
        href="/workshop/graphics/merglobe.png" title="Mercury"/>
      <area shape="circle" coords="124,58,8"
        href="/workshop/graphics/venglobe.png" title="Venus"/>
      <area shape="circle" coords="162,58,10"
        href="/workshop/graphics/earglobe.png" title="Earth"/>
      <area shape="circle" coords="203,58,8"
        href="/workshop/graphics/marglobe.png" title="Mars"/>
      <area shape="poly" coords="221,34,238,37,257,32,278,44,284,60,
        281,75,288,91,267,87,253,89,237,81,229,64,228,54"
        href="/workshop/graphics/jupglobe.png" title="Jupiter"/>
      <area shape="poly" coords="288,19,316,39,330,37,348,47,351,66,
        349,74,367,105,337,85,324,85,307,77,303,60,307,50"
        href="/workshop/graphics/satglobe.png" title="Saturn"/>
      <area shape="poly" coords="405,39,408,50,411,57,410,71,404,78,
        393,80,383,86,381,75,376,69,376,56,380,48,393,44"
        href="/workshop/graphics/uraglobe.png" title="Uranus"/>
      <area shape="poly" coords="445,38,434,49,431,53,427,62,430,72,
        435,77,445,92,456,77,463,72,463,62,462,53,455,47"
        href="/workshop/graphics/nepglobe.png" title="Neptune"/>
      <area shape="circle" coords="479,66,3"
        href="/workshop/graphics/pluglobe.png" title="Pluto"/>
  </map>
</body>
</html>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/imagemap.htm)

## Notes

### Remarks

Any number of **area** elements can be contained within the same **map** element. The format of the [**coords**](/html/attributes/coords) value depends on the value of the [**shape**](/html/attributes/shape) attribute. Windows Internet Explorer 8 and later. In IE8 Standards mode, the [**title**](/html/attributes/title) attribute is preferred over the [**alt**](/html/attributes/alt) attribute when specified as a pop-up tooltip for an **img** or a **map** element. In addition, the value of the [**href**](/html/attributes/href) attribute depends on the current document compatibility mode. This element is not rendered. This element does not require a closing tag.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/embedded-content.html#the-area-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/embedded-content-0.html#the-area-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/objects.html#edef-AREA)
:   W3C Recommendation
