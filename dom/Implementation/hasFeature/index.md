---
title: hasFeature
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'general clean-up/more description'
summary: 'Returns whether a specific DOM standard is implemented.'
uri: dom/Implementation/hasFeature

---
# hasFeature

## Summary

Returns whether a specific DOM standard is implemented.

*Method of [dom/Implementation](/dom/Implementation)*

## Syntax

``` {.js}
var featureImplemented = implementation.hasFeature(feature, version);
```

## Parameters

### feature

 Data-typeÂ
:   String

 The name of the standard. Case insensitive.

### version

 Data-typeÂ
:   String

 The version number of the standard.

## Return Value

Returns an object of type Boolean.

Whether the feature is implemented.

## Examples

The following example uses the **hasFeature** method to test whether the object implements the DOM HTML standard.

``` {.js}
var featureImplemented = document.implementation.hasFeature("HTML", "1.0");
```

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

