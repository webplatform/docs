---
title: 'data'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/CompositionEvent
    href: /dom/CompositionEvent
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/CompositionEvent
standardization_status: 'W3C Working Draft'
summary: 'Gets the text affected by the composition event.'
tags:
  - API_Object_Properties
  - DOM
uri: dom/CompositionEvent/data

---
## Summary

Gets the text affected by the composition event.

Property of [dom/CompositionEvent](/dom/CompositionEvent)[dom/CompositionEvent](/dom/CompositionEvent)

## Syntax

**Note**: This property is read-only.

``` js
var compositionData = event.html/elements/data;
```

## Return Value

Returns an object of type StringString

The text affected by the event. See the notes for event specific values.

## Examples

``` js
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

[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard

## See also

### Related pages

-   TextEvent[TextEvent](/dom/TextEvent)
