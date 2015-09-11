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
## <span>Summary</span>

Adds a new CSS rule to the stylesheet.

Method of [css/cssom/styleSheet](/css/cssom/styleSheet)[css/cssom/styleSheet](/css/cssom/styleSheet)

## <span>Syntax</span>

``` js
var index = stylesheet.insertRule(ruleText, index);
```

## <span>Parameters</span>

### <span>ruleText</span>

 Data-type
:   String

 The at-identifier ("@*rule\_name*") and the rule content.

### <span>index</span>

 Data-type
:   Number

 The index within the style sheet's rule list of the rule before which to insert the specified rule. If the specified index equals the length of the style sheet's rule list, the rule will be added to the end of the style sheet.

## <span>Return Value</span>

Returns an object of type NumberNumber

The newly inserted rule's index within the style sheet's rule list.

**Needs Examples**: This section should include examples.

## <span>Notes</span>

After the new rule has been inserted, it becomes part of the cascade.

## <span>Related specifications</span>

[DOM Level 2 Style](http://www.w3.org/TR/2000/REC-DOM-Level-2-Style-20001113/css.html)
:   Recommendation

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `styleSheet`
-   `Reference`
-   `cssRules`
-   `deleteRule`
