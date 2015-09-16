---
title: 'g'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/09f7ebf9fa8ed1d9b0d6'
compatibility:
  feature: g
  topic: svg
notes:
  - 'Needs spec reference, standardization status, fix broken link'
overview_table:
  '[DOM Interface](/dom/interface)': '[SVGElement](/svg/objects/SVGElement)'
readiness: 'In Progress'
summary: 'The g element (&lt;g&gt;) is a container element for grouping together related graphics elements.'
tags:
  - Markup
  - Elements
  - SVG
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - svg/attributes/id
uri: svg/elements/g

---
## Summary

The g element (&lt;g&gt;) is a container element for grouping together related graphics elements.

## Overview Table

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

The **g** element (\<g\>) groups two or more graphics elements or other **g** elements together to provide document structure. Groups containing the [**desc**](/svg/elements/desc) and [**title**](/svg/elements/title) elements, provide additional semantic information and increase accessibility. When defined inside of a [**defs**](/svg/elements/defs) element and named using the [**id**](/w/index.php?title=svg/attributes/id&action=edit&redlink=1) attribute, groups can be reused.

## Examples

In the following code example, the g element is used to group two elements together. They are then rotated together.

``` html


<!DOCTYPE HTML>
<html>
  <head></head>
  <body>
    <svg width="400" height="400">
      <g transform="rotate(30 75 50)">
        <rect x="50" y="50" width="50" height="50" fill="firebrick"/>
        <ellipse cx="100" cy="50" rx="25" ry="50" fill="dodgerblue"/>
      </g>
    </svg>
  </body>
</html>
```

</pre>
[View live example](http://code.webplatform.org/gist/09f7ebf9fa8ed1d9b0d6)

## Notes

### Remarks

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

### Standards information

-   [Scalable Vector Graphics: Document Structure](http://go.microsoft.com/fwlink/p/?linkid=204733), Section 5.11.3

### Members

The **SVGGElement** object has these events:

-   [**onload**](/svg/events/load): Occurs when the browser has fully parsed the element and all of its descendants.

The **SVGGElement** object has these methods:

-   [**getBBox**](/svg/methods/getBBox): Gets the bounding box, in current user space, of the geometry of all contained graphics elements.
-   [**getCTM**](/svg/methods/getCTM): Gets the transformation matrix that transforms from the current user units to the viewport coordinate system for the [**nearestViewportElement**](/svg/properties/nearestViewportElement) object.
-   [**getScreenCTM**](/svg/methods/getScreenCTM): Gets the transformation matrix from the current user units to the screen coordinate system.
-   [**getTransformToElement**](/svg/methods/getTransformToElement): Gets the transformation matrix that transforms from the user coordinate system on the current element to the user coordinate system on the specified target element.
-   [**hasExtension**](/svg/methods/hasExtension): Determines if the specified extension is supported.

The **SVGGElement** object has these properties:

-   [**className**](/svg/properties/className): Gets the names of the classes that are assigned to this object.
-   [**clipPath**](/svg/properties/clipPath): Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
-   [**externalResourcesRequired**](/svg/properties/externalResourcesRequired): Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
-   [**farthestViewportElement**](/svg/properties/farthestViewportElement): Gets a value that represents the farthest ancestor [**svg**](/svg/elements/svg) element.
-   [**focusable**](/svg/properties/focusable): Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when a user presses the Tab key).
-   [**mask**](/svg/attributes/mask): Sets or retrieves a value that indicates a SVG mask.
-   [**nearestViewportElement**](/svg/properties/nearestViewportElement): Gets a value that indicates which element established the current viewport.
-   [**ownerSVGElement**](/svg/properties/ownerSVGElement): Gets the nearest ancestor [**svg**](/svg/objects/SVGElement) element.
-   [**requiredExtensions**](/svg/properties/requiredExtensions): Gets a white space-delimited list of required language extensions.
-   [**requiredFeatures**](/svg/properties/requiredFeatures): Gets or sets a white space-delimited list of feature strings.
-   [**style**](/svg/properties/style): Gets a [**style**](/css/cssom/style) object.
-   [**systemLanguage**](/svg/properties/systemLanguage): Gets or sets a comma-separated list of language names.
-   [**transform**](/svg/properties/transform): Gets the value of a [**transform**](/svg/properties/transform) attribute.
-   [**viewportElement**](/svg/properties/viewportElement): Gets the element that established the current viewport.
-   [**xmlbase**](/svg/properties/xmlbase): Gets or sets the **base** attribute on the element.
-   [**xmllang**](/svg/properties/xmllang): Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
-   [**xmlspace**](/svg/properties/xmlspace): Gets or sets a value that indicates whether white space is preserved in character data.
