---
title: onzoom
tags:
  - Events
readiness: 'In Progress'
notes:
  - 'Needs summary, example, spec reference, standardization status'
uri: svg/events/onzoom
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/objects/Event

---
# onzoom

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

Synchronous
:   No
Bubbles
:   No
Target
:   dom/Element
Cancelable
:   No
Default action
:    ?

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The **onzoom** event occurs when the zoom level of a document view is changed through a direct user interaction or any change to the [**currentScale**](/svg/properties/currentScale) property that is available on the [**svg**](/svg/elements/svg) element. This event applies only to the outermost **svg** element and is dispatched after the zoom-level modification occurs.

Changes the document's zoom level or [**currentScale**](/svg/properties/currentScale) property. To invoke this event, do one of the following:

-   The user changes the zoom level of the document or the value of the [**svg**](/svg/elements/svg) element's [**currentScale**](/svg/properties/currentScale) property.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Scripting](http://go.microsoft.com/fwlink/p/?linkid=204745), Section 18.4.3

### Event handler parameters

*pEvt* [in]
:   Type: **IDOMUIEvent**The [**IDOMEvent**](/w/index.php?title=dom/objects/Event&action=edit&redlink=1) object.

## See also

### Related pages (MSDN)

-   [**SVGSVGElement**](/svg/elements/svg)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

