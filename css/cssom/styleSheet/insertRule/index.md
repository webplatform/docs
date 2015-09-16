---
title: insertRule
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
  return_type:
    predicate: 'Returns an object of type  '
    value: Number
    href: /css/cssom/styleSheet
standardization_status: 'W3C Recommendation'
summary: 'Adds a new CSS rule to the stylesheet.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: css/cssom/styleSheet/insertRule

---
## Summary

Adds a new CSS rule to the stylesheet.

Method of [css/cssom/styleSheet](/css/cssom/styleSheet)[css/cssom/styleSheet](/css/cssom/styleSheet)

## Syntax

``` js
var index = stylesheet.insertRule(ruleText, index);
```

## Parameters

### ruleText

 Data-type
:   String

 The at-identifier ("@*rule\_name*") and the rule content.

### index

 Data-type
:   Number

 The index within the style sheet's rule list of the rule before which to insert the specified rule. If the specified index equals the length of the style sheet's rule list, the rule will be added to the end of the style sheet.

## Return Value

Returns an object of type NumberNumber

The newly inserted rule's index within the style sheet's rule list.

**Needs Examples**: This section should include examples.

## Notes

After the new rule has been inserted, it becomes part of the cascade.

## Related specifications

[DOM Level 2 Style](http://www.w3.org/TR/2000/REC-DOM-Level-2-Style-20001113/css.html)
:   Recommendation

## See also

### Related pages (MSDN)

-   `styleSheet`
-   `Reference`
-   `cssRules`
-   `deleteRule`
