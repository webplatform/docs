---
title: 'appMinorVersion'
attributions:
  - 'Microsoft Developer Network: [[navigator.appMinorVersion](http://msdn.microsoft.com/en-us/library/ie/ms533078(v=vs.85).aspx) Article]'
code_samples:
  - 'http://result.dabblet.com/gist/b1e7c611e97594b60956/56337717d0b88e99b8944707d60bb7072b359788'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Navigator
    href: /dom/Navigator
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/Navigator
summary: 'Retrieves the userAgent application''s minor version value.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Navigator/appMinorVersion

---
## Summary

Retrieves the userAgent application's minor version value.

Property of [dom/Navigator](/dom/Navigator)[dom/Navigator](/dom/Navigator)

## Syntax

**Note**: This property is read-only.

``` js
var result = navigator.appMinorVersion;
```

## Return Value

Returns an object of type StringString

The userAgent application's minor version number.

## Examples

The linked example enumerates the window.navigator object and displays the results on the screen.

``` js

```

[View live example](http://result.dabblet.com/gist/b1e7c611e97594b60956/56337717d0b88e99b8944707d60bb7072b359788)

## Usage

     Do not use to try to detect the userAgent version number... this is unreliable.

Use 'feature detection' instead.

### Syntax
