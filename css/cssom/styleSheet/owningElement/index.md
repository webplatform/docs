---
title: owningElement
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Non-standard; deletion candidate'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/cssom/styleSheet
    href: /css/cssom/styleSheet
  return:
    predicate: 'Returns an object of type '
    value: 'DOM Node'
    href: /css/cssom/styleSheet
summary: 'Non standard. Returns the style or link object that defined the style sheet.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: css/cssom/styleSheet/owningElement

---
## <span>Summary</span>

Non standard. Returns the style or link object that defined the style sheet.

Property of [css/cssom/styleSheet](/css/cssom/styleSheet)[css/cssom/styleSheet](/css/cssom/styleSheet)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var element = stylesheet.owningElement;
```

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

The **owningElement** property returns the **style** or **link** object that defined the style sheet.

**Needs Examples**: This section should include examples.

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `styleSheet`
