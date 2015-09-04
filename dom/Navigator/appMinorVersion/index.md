---
title: appMinorVersion
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
summary: 'Retrieves the userAgent application''s minor version value.'
code_samples:
  - 'http://result.dabblet.com/gist/b1e7c611e97594b60956/56337717d0b88e99b8944707d60bb7072b359788'
uri: dom/Navigator/appMinorVersion

---
# appMinorVersion

## Summary

Retrieves the userAgent application's minor version value.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Navigator](/dom/Navigator)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = navigator.appMinorVersion;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The userAgent application's minor version number.

## Examples

The linked example enumerates the window.navigator object and displays the results on the screen.

``` {.js}
```

[View live example](http://result.dabblet.com/gist/b1e7c611e97594b60956/56337717d0b88e99b8944707d60bb7072b359788)

## Usage

     Do not use to try to detect the userAgent version number... this is unreliable.

Use 'feature detection' instead.

### Syntax

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[navigator.appMinorVersion](http://msdn.microsoft.com/en-us/library/ie/ms533078(v=vs.85).aspx) Article]

