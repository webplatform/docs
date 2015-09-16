---
title: deleteRule
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: css/cssom/styleSheet
    href: /css/cssom/styleSheet
standardization_status: 'W3C Recommendation'
summary: 'Deletes a CSS rule from the style sheet.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: css/cssom/styleSheet/deleteRule

---
## Summary

Deletes a CSS rule from the style sheet.

Method of [css/cssom/styleSheet](/css/cssom/styleSheet)[css/cssom/styleSheet](/css/cssom/styleSheet)

## Syntax

``` js
 stylesheet.deleteRule(index);
```

## Parameters

### index

 Data-type
:   Number

 The index within the rule list for the style sheet of the rule to remove.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Related specifications

[DOM Level 2 Style](http://www.w3.org/TR/2000/REC-DOM-Level-2-Style-20001113/css.html)
:   Recommendation

## See also

### Related pages (MSDN)

-   `styleSheet`
-   `Reference`
-   `cssRules`
-   `insertRule`
