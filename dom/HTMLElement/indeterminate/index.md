---
title: indeterminate
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, examples, compatibility, standards, clean-up of MSDN import'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLElement/indeterminate

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## <span>Syntax</span>

``` js
var result = element.indeterminate;
element.indeterminate = value;
```

**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

The **indeterminate** property can be used to indicate whether the user has acted on a control. For example, setting the **indeterminate** to **true** causes the check box to appear checked and dimmed, indicating an indeterminate state. The value of the **indeterminate** property acts independently of the value of the [**checked**](/html/attributes/checked) property. Creating an indeterminate state is different from disabling the control. Consequently, a check box in the indeterminate state can still receive the focus. When the user clicks an indeterminate control, the indeterminate state turns off and the checked state of the check box toggles.

### <span>Syntax</span>

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `input type=checkbox`
