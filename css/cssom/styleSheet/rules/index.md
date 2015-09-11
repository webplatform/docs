---
title: rules
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/cssom/styleSheet
    href: /css/cssom/styleSheet
summary: 'A collection of rules in a document''s stylesheet.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: css/cssom/styleSheet/rules

---
## <span>Summary</span>

A collection of rules in a document's stylesheet.

Property of [css/cssom/styleSheet](/css/cssom/styleSheet)[css/cssom/styleSheet](/css/cssom/styleSheet)

## <span>Syntax</span>

``` js
var result = element.rules;
element.rules = value;
```

**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

This collection is always accessible, even if the style sheet is not enabled. Rules are added to the [**rules**](/css/cssom/rules) collection with the [**addRule**](/css/cssom/methods/addRule) method on the individual style sheet. A rule that is added to a [**disabled**](/html/attributes/disabled) style sheet does not apply to the document unless the style sheet is enabled. Rules are deleted with the [**removeRule**](/css/cssom/methods/removeRule) method. The rules in this collection are in the source order of the document. As rules are added or deleted through the Cascading Style Sheets (CSS) Object Model, a rule's absolute position in the [**rules**](/css/cssom/rules) collection might change, but its position relative to other rules remains the same. When you add rules without specifying an index, the rule gets added to the document last. If you specify an index, however, the rule is inserted before the rule currently in that ordinal position in the collection. If the specified index is greater than the number of rules in the collection, the rule is added to the end.

### <span>Syntax</span>

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `styleSheet`
