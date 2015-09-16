---
title: hasFeature
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'general clean-up/more description'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Implementation
    href: /dom/Implementation
  return_type:
    predicate: 'Returns an object of type  '
    value: Boolean
    href: /dom/Implementation
standardization_status: 'W3C Recommendation'
summary: 'Returns whether a specific DOM standard is implemented.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Implementation/hasFeature

---
## Summary

Returns whether a specific DOM standard is implemented.

Method of [dom/Implementation](/dom/Implementation)[dom/Implementation](/dom/Implementation)

## Syntax

``` js
var featureImplemented = implementation.hasFeature(feature, version);
```

## Parameters

### feature

 Data-type
:   String

 The name of the standard. Case insensitive.

### version

 Data-type
:   String

 The version number of the standard.

## Return Value

Returns an object of type BooleanBoolean

Whether the feature is implemented.

## Examples

The following example uses the **hasFeature** method to test whether the object implements the DOM HTML standard.

``` js
var featureImplemented = document.implementation.hasFeature("HTML", "1.0");
```

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
