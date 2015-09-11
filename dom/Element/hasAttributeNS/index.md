---
title: hasAttributeNS
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example and compat table'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Element
    href: /dom/Element
  return_type:
    predicate: 'Returns an object of type  '
    value: Boolean
    href: /dom/Element
standardization_status: 'W3C Recommendation'
summary: 'Determines whether a content attribute in a specified namespace exists on an element.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Element/hasAttributeNS

---
## <span>Summary</span>

Determines whether a content attribute in a specified namespace exists on an element.

Method of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## <span>Syntax</span>

``` js
var attributeExists = element.hasAttributeNS(namespaceURI, name);
```

## <span>Parameters</span>

### <span>namespaceURI</span>

 Data-type
:   String

 The namespace URI that defines the attribute name, or null.

### <span>name</span>

 Data-type
:   String

 The name of the attribute.

## <span>Return Value</span>

Returns an object of type BooleanBoolean

Whether the specified attribute exists.

**Needs Examples**: This section should include examples.

## <span>Usage</span>

     Use this method to determine whether a content attribute in a specified namespace exists on an element.

## <span>Notes</span>

-   This method does not get the value of the attribute, see [getAttributeNS](/dom/Element/getAttributeNS) for this purpose.
-   Where namespaces are irrelevant, [hasAttribute](/dom/Element/hasAttribute) can be used instead.
-   See [hasAttributes](/dom/Node/hasAttributes), which determines whether the element has any attributes at all.

## <span>Related specifications</span>

[Document Object Model (DOM) Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

[Document Object Model (DOM) Level 2 Core](http://www.w3.org/TR/DOM-Level-2-Core/)
:   Recommendation

[DOM](http://dom.spec.whatwg.org/)
:   Living Standard
