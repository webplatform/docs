---
title: animationStartTime
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: Deprecated
notes:
  - "Not part of user_timing, resource_timing, or navigation_timing interfaces.\nsee http://www.w3.org/TR/animation-timing/"
summary: 'Obsolete. Returns a timestamp of the start time of the current refresh interval, such that multiple animations can be synchronized with each other.'
uri: dom/Window/animationStartTime

---
# animationStartTime

## Summary

Obsolete. Returns a timestamp of the start time of the current refresh interval, such that multiple animations can be synchronized with each other.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Window](/dom/Window)</span></span>

## Syntax

``` {.js}
var result = element.animationStartTime;
element.animationStartTime = value;
```

## Notes

### Remarks

Obsolete. Originally supported in pre-release versions of Internet Explorer 10, the **animationStartTime** property is superceded in favor of the **performance.now** property. Applications using **animationStartTime** should be updated accordingly. Use the *animationStartTime* property instead of recording animation start time using the **Date.now** function in order to ensure that the clock you are using has millisecond resolution and is monotonically increasing (where later values are always larger than earlier values). The value reported by the *animationStartTime* property represents the number of milliseconds between the recorded time and midnight January 1, 1970 (UTC).

### Syntax

### Standards information

-   [Timing control for script-based animations](http://go.microsoft.com/fwlink/p/?linkid=229562)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[mozAnimationStartTime](https://developer.mozilla.org/en-US/docs/Web/API/Window.mozAnimationStartTime) Article]

Portions of this content come from the Microsoft Developer Network: [[animationStartTime Property](http://msdn.microsoft.com/en-us/library/ie/hh972901(v=vs.85).aspx) Article]

