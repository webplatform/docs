---
title: object
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLAppletElement
    href: /dom/HTMLAppletElement
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/HTMLAppletElement
standardization_status: 'W3C Recommendation'
summary: 'Retrieves the contained object.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLAppletElement/object

---
## Summary

Retrieves the contained object.

Property of [dom/HTMLAppletElement](/dom/HTMLAppletElement)[dom/HTMLAppletElement](/dom/HTMLAppletElement)

## Syntax

**Note**: This property is read-only.

``` js
var result = applet.object;
```

## Return Value

Returns an object of type StringString

The applet object.

**Needs Examples**: This section should include examples.

## Usage

     If the control's object model uses a conflicting namespace, precede the control's property with object to resolve the conflict.

## Related specifications

[DOM Level 1](http://www.w3.org/TR/REC-DOM-Level-1/)
:   Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/)
:   Recommendation (deprecated usage)

## See also

### Related pages

-   `object`
-   `applet`
