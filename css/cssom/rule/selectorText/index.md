---
title: 'selectorText'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, example, spec reference, standardization status'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/cssom/rule
    href: /css/cssom/rule
tags:
  - API_Object_Properties
  - DOM
  - Needs_Summary
  - Needs_Examples
uri: css/cssom/rule/selectorText

---
Property of [css/cssom/rule](/css/cssom/rule)[css/cssom/rule](/css/cssom/rule)

## Syntax

``` js
var result = element.selectorText;
element.selectorText = value;
```

## Notes

### Remarks

Selector text can contain either a simple selector (such as 'H1') or a contextual selector (such as 'P EM') that consists of several simple selectors. Compound selectors (such as 'B, STRONG') are stored as separate rules in the collection.

### Syntax

## See also

### Related pages

-   rule[rule](/css/cssom/rule)
-   `<b/>`
-   `IHTMLStyleSheetRulesCollection`
-   rules[rules](/css/cssom/rules)
