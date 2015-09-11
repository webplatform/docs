---
title: getAttributeNS
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs compat table'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Element
    href: /dom/Element
  return_type:
    predicate: 'Returns an object of type  '
    value: String
    href: /dom/Element
standardization_status: 'W3C Recommendation'
summary: 'Returns the value of the content attribute within a specified namespace.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Element/getAttributeNS

---
## <span>Summary</span>

Returns the value of the content attribute within a specified namespace.

Method of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## <span>Syntax</span>

``` js
var attributeValue = element.getAttributeNS(namespaceURI, name);
```

## <span>Parameters</span>

### <span>namespaceURI</span>

 Data-type
:   String

 The namespace URI that defines the desired attribute, or a null value.

### <span>name</span>

 Data-type
:   String

 The name of the desired attribute within the specified namespace.

## <span>Return Value</span>

Returns an object of type StringString

The value of the content attribute, or null if it does not exist.

## <span>Examples</span>

``` js
// Get the first div element in the page.
var element = document.querySelector("div");
// Continue only if the element exists.
if (element) {
 console.log("The value of the data-example attribute of the first div is " + element.getAttributeNS("html", "data-example"));
}
```

### <span>Syntax</span>

### <span>Standards information</span>

-   [Document Object Model (DOM) Level 3 Core Specification](http://go.microsoft.com/fwlink/p/?linkid=182717), Section 1.4

## <span>Related specifications</span>

[Document Object Model (DOM) Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

[Document Object Model (DOM) Level 2 Core](http://www.w3.org/TR/DOM-Level-2-Core/)
:   Recommendation

[DOM](http://dom.spec.whatwg.org/)
:   Living Standard

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `getAttribute`
