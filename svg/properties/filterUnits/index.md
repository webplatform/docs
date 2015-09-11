---
title: filterUnits
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - svg/properties/filterUnits/svg/elements/filter
uri: svg/properties/filterUnits

---
**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

**filterUnits** defines the coordinate system for the filter attributes x, y, width and height. If **filterUnits="userSpaceOnUse"**, all attributes represent values in the current user coordinate system that is in place at the time when the filter is referenced.

If **filterUnits="objectBoundingBox"**, then all attributes represent fractions or percentages of the bounding box on the referencing element.

If attribute **filterUnits** is not specified, then the effect is the same as specifying a value of **objectBoundingBox**.

### <span>Syntax</span>

### <span>Standards information</span>

-   [<http://www.w3.org/TR/SVG11/filters.html>

## <span>See also</span>

### <span>Related pages</span>

Please see [documentation on the filter element](/w/index.php?title=svg/properties/filterUnits/svg/elements/filter&action=edit&redlink=1) for more context and examples on how to use the filterUnits property.

-   [**SVGFilterElement**](/svg/elements/filter)
