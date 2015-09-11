---
title: appendItem
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'No editing form'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/methods/appendItem

---
## <span>Notes</span>

### <span>Remarks</span>

If the *newItem* item is already in the list, the **appendItem** method removes the item from its previous list before inserting it into this list. The inserted item is the item itself and not a copy.

### <span>Syntax</span>

    ISVGTransform retVal = object.appendItem(newItem);

### <span>Standards information</span>

-   [Scalable Vector Graphics: Basic Data Types and Interfaces](http://go.microsoft.com/fwlink/p/?linkid=204732), Section 4.5.4

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   [**SVGLengthList**](/svg/objects/SVGLengthList)
-   [**SVGNumberList**](/svg/objects/SVGNumberList)
-   [**SVGPathSegList**](/svg/objects/SVGPathSegList)
-   [**SVGPointList**](/svg/objects/SVGPointList)
-   [**SVGStringList**](/svg/objects/SVGStringList)
-   [**SVGTransformList**](/svg/objects/SVGTransformList)
