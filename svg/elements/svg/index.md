---
title: svg
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, example, spec reference, standardization status'
overview_table:
  '[DOM Interface](/dom/interface)': '[SVGElement](/svg/objects/SVGElement)'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'The &lt;svg&gt; element represents the root of a Scalable Vector Graphics (SVG) fragment.'
tags:
  - Markup
  - Elements
  - SVG
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'HTML/Canvas and SVG'
uri: svg/elements/svg

---
## Summary

The &lt;svg&gt; element represents the root of a Scalable Vector Graphics (SVG) fragment.

## Overview Table

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

## Examples

``` html

<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100">
  <circle cx="50" cy="50" r="40"
      fill="red" stroke="blue" stroke-width="5" />
</svg>

```

## Usage

     Scalable Vector Graphics (SVG) is a modularized language for describing two-dimensional vector and mixed vector/raster graphics in XML. Only a correct HTML5 parser, using the syntax defined in 8 The HTML syntax, will be able to properly interpret SVG elements when using text/html. When using application/xhtml+xml, one must use proper namespaces to ensure that SVG elements are interpreted correctly.

## Notes

### Remarks

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

If an SVG document is likely to be referenced as a component of another document, you might want to include a [**viewBox**](/svg/properties/viewBox) attribute on the outermost **svg** element of the referenced document. This attribute provides a convenient way to design SVG documents to scale-to-fit into an arbitrary viewport.

**svg** elements can appear in the middle of SVG content. You can use these elements to embed SVG document fragments within other SVG document fragments. You can also use **svg** elements within the middle of SVG content to establish a new viewport.

In all cases, you must declare an SVG namespace so that all SVG elements are identified as belonging to the SVG namespace. Typically, you can declare an SVG namespace as follows:

    <svg xmlns="http://www.w3.org/2000/svg" ... >

## See also

### Other articles

-   [List of SVG Elements](/svg/elements)
-   [A comparison of canvas and SVG](/w/index.php?title=HTML/Canvas_and_SVG&action=edit&redlink=1)

### External resources

-   [Scalable Vector Graphics (SVG) 1.1](http://www.w3.org/TR/SVG11/)
