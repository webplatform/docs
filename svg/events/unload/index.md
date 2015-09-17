---
title: 'unload'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, example, spec reference, standardization status'
readiness: 'In Progress'
tags:
  - Events
  - Needs_Summary
  - Needs_Examples
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/objects/Event
    - dom/events/unload
uri: svg/events/unload

---
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
## Notes

### Remarks

The **onunload** event occurs when the DOM implementation removes a document from a window or frame. This event applies only to the outermost [**svg**](/svg/elements/svg) element.

The object or document is removed from the browser window. To invoke this event, do one of the following:

-   The DOM implementation removes a document from a window or frame.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Scripting](http://go.microsoft.com/fwlink/p/?linkid=204745), Section 18.4.3

### Event handler parameters

*pEvt* [in]
:   Type: **IDOMUIEvent**The [**IDOMEvent**](/w/index.php?title=dom/objects/Event&action=edit&redlink=1) object.

## See also

### Related pages

-   [**SVGSVGElement**](/svg/elements/svg)
-   [**onunload**](/w/index.php?title=dom/events/unload&action=edit&redlink=1)
