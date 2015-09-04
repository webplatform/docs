---
title: lengthComputable
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'needs example'
summary: 'Specifies whether the total size of the operation is known.'
uri: dom/ProgressEvent/lengthComputable

---
# lengthComputable

## Summary

Specifies whether the total size of the operation is known.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/ProgressEvent](/dom/ProgressEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = ProgressEvent.lengthComputable;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

The ProgressEvent.lengthComputable read-only property is a Boolean flag indicating if the resource concerned by the ProgressEvent has a length that can be calculated. If not, the ProgressEvent.total property has no significant value.

**Needs Examples**: This section should include examples.

### Syntax

flag = ProgressEvent.lengthComputable

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[ProgressEvent.lengthComputable](https://developer.mozilla.org/en-US/docs/Web/API/ProgressEvent.lengthComputable) Article]

Portions of this content come from the Microsoft Developer Network: [[lengthComputable Property](http://msdn.microsoft.com/en-us/library/ie/hh772354(v=vs.85).aspx) Article]

