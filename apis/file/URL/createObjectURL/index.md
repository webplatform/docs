---
title: createObjectURL
tags:
  0: API
  1: Object
  2: Methods
  4: FileAPI
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Creates a URL for the specified object.'
code_samples:
  - 'http://jsbin.com/kupizeriheci/1/edit?html,js,output'
uri: apis/file/URL/createObjectURL

---
# createObjectURL

## Summary

Creates a URL for the specified object.

*Method of [apis/file/URL](/apis/file/URL)*

## Syntax

``` {.js}
var objectURL = URL.createObjectURL(object, options);
```

## Parameters

### object

 Data-typeÂ
:   function

 The object that needs a URL. Usually a [File](/apis/file/File).

### options

 Data-typeÂ
:   DOM Node

*(Optional)*

A dictionary object. See [ObjectURLOptions](/apis/file/ObjectURLOptions) for more information. Used with *oneTimeOnly* attribute to create a single use URL that does not need to be revoked.

## Return Value

Returns an object of type String.

A URL for the specified object.

## Examples

Displaying an image based on the selected file in a `<input type=file>`

``` {.js}
var url = URL.createObjectURL(inputElement.files[0]);
imgElement.src = url;
```

[View live example](http://jsbin.com/kupizeriheci/1/edit?html,js,output)

## Notes

The URL that is created can be used for resources for use with elements such as **Image**, **video**, and **audio**. The object passed in through *object* is stored in an internal hash table. *oOptions* is set when you want to only use the URL once. The [ObjectURLOptions](/apis/file/ObjectURLOptions) object has one property, *oneTimeOnly*, that is set to *false* by default. To set the URL for the object (blob, stream, and so forth) to single use, use the ObjectURLOptions object and set *oneTimeOnly* to *true*. To revoke a URL created with createObjectURL, use [revokeObjectURL](/apis/file/URL/revokeObjectURL).

## Related specifications

Specification
:   Status
[W3C File API Specification](http://www.w3.org/TR/FileAPI)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

