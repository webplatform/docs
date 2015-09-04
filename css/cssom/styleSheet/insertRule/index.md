---
title: insertRule
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs example'
summary: 'Adds a new CSS rule to the stylesheet.'
uri: css/cssom/styleSheet/insertRule

---
# insertRule

## Summary

Adds a new CSS rule to the stylesheet.

*Method of [css/cssom/styleSheet](/css/cssom/styleSheet)*

## Syntax

``` {.js}
var index = stylesheet.insertRule(ruleText, index);
```

## Parameters

### ruleText

 Data-typeÂ
:   String

 The at-identifier ("@*rule\_name*") and the rule content.

### index

 Data-typeÂ
:   Number

 The index within the style sheet's rule list of the rule before which to insert the specified rule. If the specified index equals the length of the style sheet's rule list, the rule will be added to the end of the style sheet.

## Return Value

Returns an object of type Number.

The newly inserted rule's index within the style sheet's rule list.

**Needs Examples**: This section should include examples.

## Notes

After the new rule has been inserted, it becomes part of the cascade.

## Related specifications

Specification
:   Status
[DOM Level 2 Style](http://www.w3.org/TR/2000/REC-DOM-Level-2-Style-20001113/css.html)
:   Recommendation

## See also

### Related pages (MSDN)

-   `styleSheet`
-   `Reference`
-   `cssRules`
-   `deleteRule`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

