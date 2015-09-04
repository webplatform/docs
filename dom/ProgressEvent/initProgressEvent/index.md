---
title: initProgressEvent
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: Deprecated
notes:
  - "Depreciated?\nsee MDN link https://developer.mozilla.org/en-US/docs/Web/API/ProgressEvent.initProgressEvent"
summary: 'Initializes the value of a ProgressEvent object.'
uri: dom/ProgressEvent/initProgressEvent

---
# initProgressEvent

## Summary

Initializes the value of a ProgressEvent object.

*Method of [dom/ProgressEvent](/dom/ProgressEvent)*

## Syntax

``` {.js}
var object = object.initProgressEvent(/* see parameter list */);
```

## Parameters

### typeArg

 Data-typeÂ
:   String

 The value of this parameter must be one of the following values. 'loadstart' An operation has started. 'progress' An operation is in progress. 'error' The operation failed to complete. 'abort' The operation was cancelled. 'load' The operation completed successfully.

### canBubbleArg

 Data-typeÂ
:   Boolean

 Specifies whether an event bubbles.

### cancelableArg

 Data-typeÂ
:   Boolean

 Specifies whether an event can be cancelled.

### lengthComputable

 Data-typeÂ
:   Boolean

 Indicates whether the value of the [**total**](/dom/ProgressEvent/total) attribute of the [**ProgressEvent**](/dom/ProgressEvent) is accurate.

### loadedArg

 Data-typeÂ
:   unsigned long

 Specifies the number of bytes already loaded or zero if not known.

### totalArg

 Data-typeÂ
:   unsigned long

 Specifies the number of bytes to be loaded. If *lengthComputable* is false, this must be zero ("0").

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

This method can return one of these values.

S\_OK

## Notes

Depreciated This feature has been removed from the Web. Though some browsers may still support it, it is in the process of being dropped. Do not use it in old or new projects. Pages or Web apps using it may break at any time.

Non-standard This feature is non-standard and is not on a standards track. Do not use it on production sites facing the Web: it will not work for every user. There may also be large incompatibilities between implementations and the behavior may change in the future.

### Syntax

var retval = ProgressEvent.initProgressEvent(typeArg, canBubbleArg, cancelableArg, lengthComputable, loadedArg, totalArg);

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[ProgressEvent.initProgressEvent](https://developer.mozilla.org/en-US/docs/Web/API/ProgressEvent.initProgressEvent) Article]

Portions of this content come from the Microsoft Developer Network: [[initProgressEvent Method](http://msdn.microsoft.com/en-us/library/ie/hh772353(v=vs.85).aspx) Article]

