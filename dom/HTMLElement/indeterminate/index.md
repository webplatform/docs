---
title: indeterminate
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Not Ready'
notes:
  - 'summary, examples, compatibility, standards, clean-up of MSDN import'
uri: dom/HTMLElement/indeterminate

---
# indeterminate

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLElement](/dom/HTMLElement)</span></span>

## Syntax

``` {.js}
var result = element.indeterminate;
element.indeterminate = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The **indeterminate** property can be used to indicate whether the user has acted on a control. For example, setting the **indeterminate** to **true** causes the check box to appear checked and dimmed, indicating an indeterminate state. The value of the **indeterminate** property acts independently of the value of the [**checked**](/html/attributes/checked) property. Creating an indeterminate state is different from disabling the control. Consequently, a check box in the indeterminate state can still receive the focus. When the user clicks an indeterminate control, the indeterminate state turns off and the checked state of the check box toggles.

### Syntax

## See also

### Related pages (MSDN)

-   `input type=checkbox`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

