---
title: locale
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs spec reference'
summary: 'Gets the locale name (language code, e.g., "en-US", "fr", "de", "ja", etc.) for the composition event, if available; otherwise, the empty string.'
uri: dom/CompositionEvent/locale

---
# locale

## Summary

Gets the locale name (language code, e.g., "en-US", "fr", "de", "ja", etc.) for the composition event, if available; otherwise, the empty string.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/CompositionEvent](/dom/CompositionEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var localeName = event.locale;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The locale of the event.

## Examples

``` {.js}
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

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

