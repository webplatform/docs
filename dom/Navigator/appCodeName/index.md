---
title: appCodeName
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
summary: 'Returns the internal "code" name of the current browser. Do not rely on this property to return the correct value.'
code_samples:
  - 'http://result.dabblet.com/gist/b1e7c611e97594b60956/56337717d0b88e99b8944707d60bb7072b359788'
uri: dom/Navigator/appCodeName

---
# appCodeName

## Summary

Returns the internal "code" name of the current browser. Do not rely on this property to return the correct value.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Navigator](/dom/Navigator)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = navigator.appCodeName;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

the internal "code" name of the current web browser.

## Examples

the linked example enumerates the navigator object, displaying each property and method on the screen.

``` {.js}
navigator.appCodeName
```

[View live example](http://result.dabblet.com/gist/b1e7c611e97594b60956/56337717d0b88e99b8944707d60bb7072b359788)

## Usage

     Should not be used to detect the current web browser vendor or "code" name.

### Syntax

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[navigator.appCodeName](https://developer.mozilla.org/en-US/docs/Web/API/NavigatorID.appCodeName) Article]

Portions of this content come from the Microsoft Developer Network: [[navigator.appCodeName](http://msdn.microsoft.com/en-us/library/ie/ms533077(v=vs.85).aspx) Article]

