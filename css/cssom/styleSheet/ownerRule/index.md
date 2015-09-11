---
title: ownerRule
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/cssom/styleSheet
    href: /css/cssom/styleSheet
  return:
    predicate: 'Returns an object of type '
    value: 'DOM Node'
    href: /css/cssom/styleSheet
standardization_status: 'W3C Recommendation'
summary: 'Gets the CSS Rule that imported the style sheet, if any.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: css/cssom/styleSheet/ownerRule

---
## <span>Summary</span>

Gets the CSS Rule that imported the style sheet, if any.

Property of [css/cssom/styleSheet](/css/cssom/styleSheet)[css/cssom/styleSheet](/css/cssom/styleSheet)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var rule = stylesheet.ownerRule;
```

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Of type CSSRule. Returns a CSSImportRule or null.

**Needs Examples**: This section should include examples.

## <span>Notes</span>

If the style sheet comes from an [**@import**](/css/atrules/@import) rule, the **ownerRule** property will contain a [**CSSImportRule**](/css/cssom/CSSImportRule) object, and the [**ownerNode**](/css/cssom/styleSheet/ownerNode) property will be `null`. If the style sheet comes from a link, the **ownerRule** property will be `null`, and the **ownerNode** will contain the node.

## <span>Related specifications</span>

[DOM Level 2 Style](http://www.w3.org/TR/2000/REC-DOM-Level-2-Style-20001113/css.html)
:   Recommendation

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `styleSheet`
-   `cssRules`
