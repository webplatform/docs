---
title: readOnly
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Not Ready'
notes:
  - 'Non-standard; deletion candidate.'
summary: 'Non standard. Indicates if the style sheet is currently in read only mode.'
uri: css/cssom/styleSheet/readOnly

---
# readOnly

## Summary

Non standard. Indicates if the style sheet is currently in read only mode.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/cssom/styleSheet](/css/cssom/styleSheet)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var isReadOnly = stylesheet.readOnly;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

Returns whether the style sheet is currently in read only mode.

**Needs Examples**: This section should include examples.

## Notes

You cannot modify style sheets obtained through a **link** object or the [**@import**](/css/atrules/@import) rule while the [**designMode**](/dom/Document/designMode) property is enabled. For more information, see Introduction to MSHTML Editing.

## See also

### Related pages (MSDN)

-   `styleSheet`
-   `rule`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

