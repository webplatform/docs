---
title: 'map'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/imagemap.htm'
compatibility:
  feature: map
  topic: html
notes:
  - 'Add Category, Parent, Children and Compatibility information. Add HTML information section.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLMapElement](/dom/HTMLMapElement)'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'Contains coordinate data for client-side image maps.'
tags:
  - Markup_Elements
  - HTML
uri: html/elements/map

---
## Summary

Contains coordinate data for client-side image maps.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLMapElement](/dom/HTMLMapElement)

An image, in the form of an img element or an object element representing an image, may be associated with an image map (in the form of a map element) by specifying a usemap attribute on the img or object element.

## Attributes

-   `name` = name of map
    Gives the map a name so that it can be referenced.
    The attribute must be present and must have a non-empty value with no space characters.
    The value of the name attribute must not be a compatibility-caseless match for the value of the name attribute of another map element in the same document.
    If the id attribute is also specified, both attributes must have the same value.

## Examples

This example provides the full code for an image map of the solar system. It creates links from the image map to individual images of the planets using the **AREA** element with the **MAP** element, [**COORDS**](/html/attributes/coords) value, and [**SHAPE**](/html/attributes/shape) attribute. The user clicks the sun or any planet to link to an individual image. To return to the solar system image map, the user clicks the **Back** button.

``` html
<img src="solarsys.png" width="504" height="126" alt="Solar System" usemap="#SystemMap"/>
<map name="SystemMap">
  <area shape="rect" coords="0,0,82,126" href="/workshop/graphics/sun.png" alt="sun"/>
  <area shape="circle" coords="90,58,3" href="/workshop/graphics/merglobe.png" alt="mercury"/>
  <area shape="circle" coords="124,58,8" href="/workshop/graphics/venglobe.png" alt="venus"/>
  <area shape="circle" coords="162,58,10" href="/workshop/graphics/earglobe.png" alt="earth"/>
  <area shape="circle" coords="203,58,8" href="/workshop/graphics/marglobe.png" alt="mars"/>
  <area shape="poly" coords="221,34,238,37,257,32,278,44,284,60,281,75,288,91,267,87,253,89,237,81,229,64,228,54" href="/workshop/graphics/jupglobe.png" alt="jupiter"/>
  <area shape="poly" coords="288,19,316,39,330,37,348,47,351,66,349,74,367,105,337,85,324,85,307,77,303,60,307,50" href="/workshop/graphics/satglobe.png" alt="saturn"/>
  <area shape="poly" coords="405,39,408,50,411,57,410,71,404,78,393,80,383,86,381,75,376,69,376,56,380,48,393,44" href="/workshop/graphics/uraglobe.png" alt="uranus"/>
  <area shape="poly" coords="445,38,434,49,431,53,427,62,430,72,435,77,445,92,456,77,463,72,463,62,462,53,455,47" href="/workshop/graphics/nepglobe.png" alt="neptune"/>
  <area shape="circle" coords="479,66,3" href="/workshop/graphics/pluglobe.png" alt="pluto"/>
</map>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/imagemap.htm)

## Notes

### Remarks

An image map is a graphic image, with predefined regions, that contains links to other documents or anchors. For example, you could create an image of the solar system containing links that the user can click to navigate to pages for the individual planets. The **map** object is referenced with the [**USEMAP**](/html/attributes/useMap) attribute in an **IMG** element, as follows:

    <img src="solarsys.png" usemap="#SystemMap">

A **MAP** element contains a set of **AREA** elements defining the linking regions in the image.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/embedded-content.html#the-map-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/embedded-content-0.html#the-map-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/objects.html#edef-MAP)
:   W3C Recommendation
