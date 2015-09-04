---
title: createControlRange
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
notes:
  - 'Needs examples, specs, and compat'
uri: dom/Element/createControlRange

---
# createControlRange

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [dom/Element](/dom/Element)*

## Syntax

``` {.js}
var object = object.createControlRange();
```

## Return Value

Returns an object of type DOM Node.

Object

Returns a [**controlRange**](/dom/HTMLElement/controlRange) collection if sucessful or a null value otherwise.

## Examples

This example creates a [**controlRange**](/dom/HTMLElement/controlRange) by using the **createControlRange** method.

    oControlRange = document.body.createControlRange();

## Notes

### Remarks

Creates a selection range object for control-based selection rather than text-based selection. If a [**controlRange**](/dom/HTMLElement/controlRange) already exists, **createControlRange** overwrites the existing element; otherwise, it returns a pointer to the element created. If there are currently controls selected in the text container, the control range is initialized with them; otherwise, it is created empty and controls need to be explicitly added to it. This is opposite of the text range, which defaults to the whole text container if there is no selection.

### Syntax

### Standards information

There are no standards that apply here.

## See also

### Related pages (MSDN)

-   `body`
-   `createRange`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

