---
title: locale
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs spec reference'
readiness: 'Almost Ready'
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
summary: 'Gets the locale name (language code, e.g., &quot;en-US&quot;, &quot;fr&quot;, &quot;de&quot;, &quot;ja&quot;, etc.) for the composition event, if available; otherwise, the empty string.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/CompositionEvent/locale

---
## Summary

Gets the locale name (language code, e.g., &quot;en-US&quot;, &quot;fr&quot;, &quot;de&quot;, &quot;ja&quot;, etc.) for the composition event, if available; otherwise, the empty string.

Property of [dom/CompositionEvent](/dom/CompositionEvent)[dom/CompositionEvent](/dom/CompositionEvent)

## Syntax

**Note**: This property is read-only.

``` js
var localeName = event.locale;
```

## Return Value

Returns an object of type StringString

The locale of the event.

## Examples

``` js
function getLocale(e) {
//retrieve locale string for composition event
var localeString = e.locale;
return localeString;
}
```

## Notes

For trusted events, the **locale** property is set for keyboard and Input Method Editor (IME) input only. The locale name is set from the default LCID of the thread, `en-US`, for example.

## See also

### Related pages (MSDN)

-   `KeyboardEvent`
-   `TextEvent`
