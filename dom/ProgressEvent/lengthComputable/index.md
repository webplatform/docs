---
title: 'lengthComputable'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[ProgressEvent.lengthComputable](https://developer.mozilla.org/en-US/docs/Web/API/ProgressEvent.lengthComputable) Article]'
  - 'Microsoft Developer Network: [[lengthComputable Property](http://msdn.microsoft.com/en-us/library/ie/hh772354(v=vs.85).aspx) Article]'
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
    value: Boolean
    href: /dom/ProgressEvent
standardization_status: 'W3C Recommendation'
summary: 'Specifies whether the total size of the operation is known.'
tags:
  - API_Object_Properties
  - DOM
  - Needs_Examples
uri: dom/ProgressEvent/lengthComputable

---
## Summary

Specifies whether the total size of the operation is known.

Property of [dom/ProgressEvent](/dom/ProgressEvent)[dom/ProgressEvent](/dom/ProgressEvent)

## Syntax

**Note**: This property is read-only.

``` js
var result = ProgressEvent.lengthComputable;
```

## Return Value

Returns an object of type BooleanBoolean

The ProgressEvent.lengthComputable read-only property is a Boolean flag indicating if the resource concerned by the ProgressEvent has a length that can be calculated. If not, the ProgressEvent.total property has no significant value.

### Syntax

flag = ProgressEvent.lengthComputable
