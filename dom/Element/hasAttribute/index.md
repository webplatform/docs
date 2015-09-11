---
title: hasAttribute
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
    value: Boolean
    href: /dom/Element
standardization_status: 'W3C Recommendation'
summary: 'Determines whether a content attribute exists on an element.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Element/hasAttribute

---
## <span>Summary</span>

Determines whether a content attribute exists on an element.

Method of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## <span>Syntax</span>

``` js
var attributeExists = element.hasAttribute(name);
```

## <span>Parameters</span>

### <span>name</span>

 Data-type
:   String

 The name of the attribute.

## <span>Return Value</span>

Returns an object of type BooleanBoolean

Whether the specified attribute exists.

## <span>Examples</span>

``` js
// Get the first div element in the page.
var element = document.querySelector("div");
// Continue only if the element exists.
if (element) {
 console.log("Does the first div have a data-example attribute? " + element.hasAttribute("data-example"));
}
```

## <span>Usage</span>

     Use this method to determine whether a content attribute exists on an element.

## <span>Notes</span>

-   This method does not get the value of the attribute, see [**getAttribute**](/dom/Element/getAttribute) for this purpose.
-   See [**hasAttributes**](/dom/Node/hasAttributes), which determines whether the element has any attributes at all.

## <span>Related specifications</span>

[Document Object Model (DOM) Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

[Document Object Model (DOM) Level 2 Core](http://www.w3.org/TR/DOM-Level-2-Core/)
:   Recommendation

[DOM](http://dom.spec.whatwg.org/)
:   Living Standard
