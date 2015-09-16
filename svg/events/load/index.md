---
title: load
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, example, spec reference, standardization status'
readiness: 'In Progress'
tags:
  - Events
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/objects/Event
uri: svg/events/load

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

<table class="wikitable">
<tr>
<th>
Synchronous

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Bubbles

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Target

</th>
<td>
dom/Element

</td>
</tr>
<tr>
<th>
Cancelable

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Default action

</th>
<td>
 ?

</td>
</tr>
</table>
**Needs Examples**: This section should include examples.

## Notes

### Remarks

The **onload** event occurs when the browser has fully parsed the element and its descendants and is ready to act appropriately on that element, such as rendering the element to the target device. Before the event occurs, the browser must have loaded, parsed, and prepared referenced external resources for rendering. Optional external resources are not required to be ready for the event to occur.

The object that the event is specified for is loaded. To invoke this event, do one of the following:

-   A user opens a page in the browser to fire this event for the document or any object within it.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Scripting](http://go.microsoft.com/fwlink/p/?linkid=204745), Section 18.4.2

### Event handler parameters

*pEvt* [in]
:   Type: **IDOMUIEvent**The [**IDOMEvent**](/w/index.php?title=dom/objects/Event&action=edit&redlink=1) object.

## See also

### Related pages (MSDN)

-   [**SVGAElement**](/svg/elements/a)
-   [**SVGCircleElement**](/svg/elements/circle)
-   [**SVGClipPathElement**](/svg/elements/clipPath)
-   [**SVGDefsElement**](/svg/elements/defs)
-   [**SVGDescElement**](/svg/elements/desc)
-   [**SVGEllipseElement**](/svg/elements/ellipse)
-   [**SVGGElement**](/svg/elements/g)
-   [**SVGGradientElement**](/svg/elements/gradient)
-   [**SVGImageElement**](/svg/elements/image)
-   [**SVGLineElement**](/svg/elements/line)
-   [**SVGMarkerElement**](/svg/elements/marker)
-   [**SVGMaskElement**](/svg/elements/mask)
-   [**SVGMetadataElement**](/svg/elements/metadata)
-   [**SVGPathElement**](/svg/elements/path)
-   [**SVGPatternElement**](/svg/elements/patterrn)
-   [**SVGPolygonElement**](/svg/elements/polygon)
-   [**SVGPolylineElement**](/svg/elements/polyline)
-   [**SVGRectElement**](/svg/elements/rect)
-   [**SVGScriptElement**](/svg/elements/script)
-   [**SVGStopElement**](/svg/elements/stop)
-   [**SVGStyleElement**](/svg/elements/style)
-   [**SVGSVGElement**](/svg/elements/svg)
-   [**SVGSwitchElement**](/svg/elements/switch)
-   [**SVGSymbolElement**](/svg/elements/symbol)
-   [**SVGTextElement**](/svg/elements/text)
-   [**SVGTSpanElement**](/svg/elements/tspan)
-   [**SVGTextPathElement**](/svg/elements/textPath)
-   [**SVGUseElement**](/svg/elements/use)
-   [**SVGViewElement**](/svg/elements/view)
