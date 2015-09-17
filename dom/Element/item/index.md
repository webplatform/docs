---
title: 'item'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, examples, syntax, compat, spec'
readiness: 'Not Ready'
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
  - API_Object_Methods
  - DOM
  - Needs_Summary
  - Needs_Examples
uri: dom/Element/item

---
Method of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## Syntax

``` js
var object = object.item(/* see parameter list */);
```

## Parameters

### index

 Data-type
:   any

 An **Integer** that specifies the zero-based index of the object to get.

## Return Value

Returns an object of type DOM NodeDOM Node

**IHTMLElement**

## Notes

### Remarks

**Note**   if given a string that is not a numeric index, this method will return the object at index `0`. This method returns S\_OK, even if the element is not found. Check the value of the IDispatch pointer returned by this call. If the value of the pointer is NULL; the element was not found, and the call was not successful.

### Syntax

### Standards information

There are no standards that apply here.
