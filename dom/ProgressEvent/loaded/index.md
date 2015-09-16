---
title: 'loaded'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[ProgressEvent.loaded](https://developer.mozilla.org/en-US/docs/Web/API/ProgressEvent.loaded) Article]'
  - 'Microsoft Developer Network: [[loaded Property](http://msdn.microsoft.com/en-us/library/ie/hh772355(v=vs.85).aspx) Article]'
notes:
  - 'needs example'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/ProgressEvent
    href: /dom/ProgressEvent
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned long'
    href: /dom/ProgressEvent
standardization_status: 'W3C Recommendation'
summary: 'Specifies the number of bytes downloaded since the beginning of the operation.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/ProgressEvent/loaded

---
## Summary

Specifies the number of bytes downloaded since the beginning of the operation.

Property of [dom/ProgressEvent](/dom/ProgressEvent)[dom/ProgressEvent](/dom/ProgressEvent)

## Syntax

**Note**: This property is read-only.

``` js
var result = ProgressEvent.loaded;
```

## Return Value

Returns an object of type unsigned longunsigned long

Number of bytes downloaded since the beginning of the operation.

**Needs Examples**: This section should include examples.

## Usage

     Used to calculate the percentage completed of an operation.

## Notes

### Remarks

This property refers to the content associated with the operation; it does not account for headers or other overhead associated with the operation. If the operation specifies content encoding or transfer encoding, the value of this property reflects the specified encoding.

### Syntax

value = ProgressEvent.loaded
