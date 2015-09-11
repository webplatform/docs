---
title: ObjectURLOptions
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Provides the oneTimeOnly property for use with the createObjectURL method.'
tags:
  0: API
  1: Objects
  3: FileAPI
uri: apis/file/ObjectURLOptions

---
## <span>Summary</span>

Provides the oneTimeOnly property for use with the createObjectURL method.

## <span>Properties</span>

*No properties.*

## <span>Methods</span>

*No methods.*

## <span>Events</span>

*No events.*

## <span>Examples</span>

``` js
oURL = URL.createObjectURL(file, {oneTimeOnly: true});
```

The **ObjectURLOptions** object provides the *oneTimeOnly* property, which specifies whether an object created with [createObjectURL](/apis/file/URL/createObjectURL) is only used once, and thus does not need [revokeObjectURL](/apis/file/URL/createObjectURL) run against it.

## <span>Related specifications</span>

[W3C File API Specification](http://www.w3.org/TR/FileAPI)
:   W3C Working Draft
