---
title: data
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Gets the text affected by the composition event.'
uri: dom/CompositionEvent/data

---
# data

## Summary

Gets the text affected by the composition event.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/CompositionEvent](/dom/CompositionEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var compositionData = event.data;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The text affected by the event. See the notes for event specific values.

## Examples

``` {.js}
function getCompEventText(e) {
//retrieve text for composition event
var compEventText = e.data;
return compEventText;
}
```

## Notes

The value varies by the event type:

-   For **compositionstart** - the text that was selected.
-   For **compositionupdate** - the current text.
-   For **compositionend** - the text that will be committed.

If a user cancels a composition event, the **data** attribute is set to null on the final **compositionupdate** event.

## Related specifications

Specification
:   Status
[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft
[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard

## See also

### Related pages (MSDN)

-   `TextEvent`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

