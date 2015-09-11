---
title: createControlRange
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs examples, specs, and compat'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Element
    href: /dom/Element
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Element
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Element/createControlRange

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## <span>Syntax</span>

``` js
var object = object.createControlRange();
```

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Object

Returns a [**controlRange**](/dom/HTMLElement/controlRange) collection if sucessful or a null value otherwise.

## <span>Examples</span>

This example creates a [**controlRange**](/dom/HTMLElement/controlRange) by using the **createControlRange** method.

``` html
oControlRange = document.body.createControlRange();
```

## <span>Notes</span>

### <span>Remarks</span>

Creates a selection range object for control-based selection rather than text-based selection. If a [**controlRange**](/dom/HTMLElement/controlRange) already exists, **createControlRange** overwrites the existing element; otherwise, it returns a pointer to the element created. If there are currently controls selected in the text container, the control range is initialized with them; otherwise, it is created empty and controls need to be explicitly added to it. This is opposite of the text range, which defaults to the whole text container if there is no selection.

### <span>Syntax</span>

### <span>Standards information</span>

There are no standards that apply here.

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `body`
-   `createRange`
