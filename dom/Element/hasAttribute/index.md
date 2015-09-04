---
title: hasAttribute
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs compat table'
summary: 'Determines whether a content attribute exists on an element.'
uri: dom/Element/hasAttribute

---
# hasAttribute

## Summary

Determines whether a content attribute exists on an element.

*Method of [dom/Element](/dom/Element)*

## Syntax

``` {.js}
var attributeExists = element.hasAttribute(name);
```

## Parameters

### name

 Data-typeÂ
:   String

 The name of the attribute.

## Return Value

Returns an object of type Boolean.

Whether the specified attribute exists.

## Examples

``` {.js}
// Get the first div element in the page.
var element = document.querySelector("div");
// Continue only if the element exists.
if (element) {
 console.log("Does the first div have a data-example attribute? " + element.hasAttribute("data-example"));
}
```

## Usage

     Use this method to determine whether a content attribute exists on an element.

## Notes

-   This method does not get the value of the attribute, see [**getAttribute**](/dom/Element/getAttribute) for this purpose.
-   See [**hasAttributes**](/dom/Node/hasAttributes), which determines whether the element has any attributes at all.

## Related specifications

Specification
:   Status
[Document Object Model (DOM) Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
[Document Object Model (DOM) Level 2 Core](http://www.w3.org/TR/DOM-Level-2-Core/)
:   Recommendation
[DOM](http://dom.spec.whatwg.org/)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

