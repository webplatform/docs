---
title: ownerRule
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs example'
summary: 'Gets the CSS Rule that imported the style sheet, if any.'
uri: css/cssom/styleSheet/ownerRule

---
# ownerRule

## Summary

Gets the CSS Rule that imported the style sheet, if any.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/cssom/styleSheet](/css/cssom/styleSheet)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var rule = stylesheet.ownerRule;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">DOM Node</span></span>

Of type CSSRule. Returns a CSSImportRule or null.

**Needs Examples**: This section should include examples.

## Notes

If the style sheet comes from an [**@import**](/css/atrules/@import) rule, the **ownerRule** property will contain a [**CSSImportRule**](/css/cssom/CSSImportRule) object, and the [**ownerNode**](/css/cssom/styleSheet/ownerNode) property will be `null`. If the style sheet comes from a link, the **ownerRule** property will be `null`, and the **ownerNode** will contain the node.

## Related specifications

Specification
:   Status
[DOM Level 2 Style](http://www.w3.org/TR/2000/REC-DOM-Level-2-Style-20001113/css.html)
:   Recommendation

## See also

### Related pages (MSDN)

-   `styleSheet`
-   `cssRules`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

