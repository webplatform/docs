---
title: parentStyleSheet
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
summary: 'Retrieves an element''s parent style sheet.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: css/cssom/styleSheet/parentStyleSheet

---
## <span>Summary</span>

Retrieves an element's parent style sheet.

Property of [css/cssom/styleSheet](/css/cssom/styleSheet)[css/cssom/styleSheet](/css/cssom/styleSheet)

## <span>Syntax</span>

``` js
var result = element.parentStyleSheet;
element.parentStyleSheet = value;
```

**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

Parameter *p* receives **NULL** if the style sheet is part of a **link** or **style** element.

### <span>Syntax</span>

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `styleSheet`
