---
title: elapsedTime
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs example... link to MSDN hands on wizard added, but a use example needed.'
summary: 'The amount of time the transition has been running, in seconds.'
code_samples:
  - 'http://ie.microsoft.com/testdrive/Graphics/hands-on-css3/hands-on_animations.htm'
uri: dom/TransitionEvent/elapsedTime

---
# elapsedTime

## Summary

The amount of time the transition has been running, in seconds.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/TransitionEvent](/dom/TransitionEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = object.elapsedTime;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

Type: Floating-point

The amount of time the transition has been running, in seconds, when this event fired.

## Examples

MSDN hands-on CSS3 Animations wizard.

[View live example](http://ie.microsoft.com/testdrive/Graphics/hands-on-css3/hands-on_animations.htm)

## Notes

### Remarks

**Note**  This value is not affected by the value of [**transition-delay**](/css/properties/transition-delay).

### Syntax

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[TransitionEvent.elapsedTime](https://developer.mozilla.org/en-US/docs/Web/API/TransitionEvent.elapsedTime) Article]

Portions of this content come from the Microsoft Developer Network: [[elapsedTime Property](http://msdn.microsoft.com/en-us/library/ie/hh772137(v=vs.85).aspx) Article]

