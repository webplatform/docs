---
title: ObjectURLOptions
tags:
  0: API
  1: Objects
  3: FileAPI
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Provides the oneTimeOnly property for use with the createObjectURL method.'
uri: apis/file/ObjectURLOptions

---
# ObjectURLOptions

## Summary

Provides the oneTimeOnly property for use with the createObjectURL method.

## Properties

*No properties.*

## Methods

*No methods.*

## Events

*No events.*

## Examples

``` {.js}
oURL = URL.createObjectURL(file, {oneTimeOnly: true});
```

The **ObjectURLOptions** object provides the *oneTimeOnly* property, which specifies whether an object created with [createObjectURL](/apis/file/URL/createObjectURL) is only used once, and thus does not need [revokeObjectURL](/apis/file/URL/createObjectURL) run against it.

## Related specifications

Specification
:   Status
[W3C File API Specification](http://www.w3.org/TR/FileAPI)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

