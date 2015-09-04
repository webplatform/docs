---
title: loaded
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'needs example'
summary: 'Specifies the number of bytes downloaded since the beginning of the operation.'
uri: dom/ProgressEvent/loaded

---
# loaded

## Summary

Specifies the number of bytes downloaded since the beginning of the operation.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/ProgressEvent](/dom/ProgressEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = ProgressEvent.loaded;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

Number of bytes downloaded since the beginning of the operation.

**Needs Examples**: This section should include examples.

## Usage

     Used to calculate the percentage completed of an operation.

## Notes

### Remarks

This property refers to the content associated with the operation; it does not account for headers or other overhead associated with the operation. If the operation specifies content encoding or transfer encoding, the value of this property reflects the specified encoding.

### Syntax

value = ProgressEvent.loaded

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[ProgressEvent.loaded](https://developer.mozilla.org/en-US/docs/Web/API/ProgressEvent.loaded) Article]

Portions of this content come from the Microsoft Developer Network: [[loaded Property](http://msdn.microsoft.com/en-us/library/ie/hh772355(v=vs.85).aspx) Article]

