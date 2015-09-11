---
title: marker
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, spec reference, standardization status'
overview_table:
  '[DOM Interface](/dom/interface)': '[SVGElement](/svg/objects/SVGElement)'
readiness: 'In Progress'
tags:
  - Markup
  - Elements
  - SVG
uri: svg/elements/marker

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

## <span>Examples</span>

In the following code example, square markers are added to each end of a path. Copy this sample to a text file and save it with the *.html* file extension. Run it in Internet Explorer 9 to see the path with two markers on the screeen.

The path with markers will look like this:

``` html


<!DOCTYPE HTML>
<html>
  <head></head>
  <body>
    <!-- Inline SVG -->
    <svg width="400" height="400">
      <!-- Definition of marker -->
      <defs>
        <marker id="knob"
                  viewBox="0 0 10 10" refX="0" refY="5"
                  markerUnits="strokeWidth"
                  markerWidth="4" markerHeight="3" orient="auto">
                  <path d="M 0 0 L 10 5 L 0 10 z" />
        </marker>
      </defs>
      <!-- Path that will have knobs at both ends -->
      <path d="M 50,100 Q 150,50 250,100" stroke="hotpink"
                stroke-width="10" fill="white"
                marker-start="url(#knob)"
                marker-end="url(#knob)" />
    </svg>
  </body>
</html>
```

</pre>

## <span>Notes</span>

### <span>Remarks</span>

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

### <span>Standards information</span>

-   [Scalable Vector Graphics: Painting, Filling, Stroking and Marker Symbols](http://go.microsoft.com/fwlink/p/?linkid=199816), Section 11.9.2

### <span>Members</span>

The **SVGMarkerElement** object has these events:

-   [**onload**](/svg/events/load): Occurs when the browser has fully parsed the element and all of its descendants.

The **SVGMarkerElement** object has these methods:

-   [**setOrientToAngle**](/svg/methods/setOrientToAngle): Sets the value of the [**orientAngle**](/svg/properties/orientAngle) attribute to the specified angle.
-   [**setOrientToAuto**](/svg/methods/setOrientToAuto): Sets the value of the **svgMarkerOrient** attribute to **auto**.

The **SVGMarkerElement** object has these properties:

-   [**className**](/svg/properties/className): Gets the names of the classes that are assigned to this object.
-   [**clipPath**](/svg/properties/clipPath): Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
-   [**externalResourcesRequired**](/svg/properties/externalResourcesRequired): Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
-   [**focusable**](/svg/properties/focusable): Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when a user presses the Tab key).
-   [**markerHeight**](/svg/properties/markerHeight): Gets the height attribute of the **marker** element.
-   [**markerUnits**](/svg/properties/markerUnits): Gets or sets the coordinate system for the [**markerWidth**](/svg/properties/markerWidth) and [**markerHeight**](/svg/properties/markerHeight) attributes and for the contents of the **marker** element.
-   [**markerWidth**](/svg/properties/markerWidth): Gets the width attribute of the **marker** element.
-   [**mask**](/svg/attributes/mask): Sets or retrieves a value that indicates a SVG mask.
-   [**orientAngle**](/svg/properties/orientAngle): Gets the angle of orientation of the **marker** element.
-   [**orientType**](/svg/properties/orientType): Gets the orientation type for a **marker** element.
-   [**ownerSVGElement**](/svg/properties/ownerSVGElement): Gets the nearest ancestor [**svg**](/svg/objects/SVGElement) element.
-   [**preserveAspectRatio**](/svg/properties/preserveAspectRatio): Gets an XML value that indicates whether to force uniform graphic scaling.
-   [**refX**](/svg/properties/refX): Gets the [**refX**](/svg/properties/refX) attribute on the **marker** element.
-   [**refY**](/svg/properties/refY): Gets the [**refY**](/svg/properties/refY) attribute on the **marker** element.
-   [**style**](/svg/properties/style): Gets a [**style**](/css/cssom/style) object.
-   [**viewBox**](/svg/properties/viewBox): Gets a value that indicates how a graphic scales to fit a container element.
-   [**viewportElement**](/svg/properties/viewportElement): Gets the element that established the current viewport.
-   [**xmlbase**](/svg/properties/xmlbase): Gets or sets the **base** attribute on the element.
-   [**xmllang**](/svg/properties/xmllang): Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
-   [**xmlspace**](/svg/properties/xmlspace): Gets or sets a value that indicates whether white space is preserved in character data.
