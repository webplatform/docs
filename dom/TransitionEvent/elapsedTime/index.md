---
title: elapsedTime
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[TransitionEvent.elapsedTime](https://developer.mozilla.org/en-US/docs/Web/API/TransitionEvent.elapsedTime) Article]'
  - 'Microsoft Developer Network: [[elapsedTime Property](http://msdn.microsoft.com/en-us/library/ie/hh772137(v=vs.85).aspx) Article]'
code_samples:
  - 'http://ie.microsoft.com/testdrive/Graphics/hands-on-css3/hands-on_animations.htm'
notes:
  - 'Needs example... link to MSDN hands on wizard added, but a use example needed.'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/TransitionEvent
    href: /dom/TransitionEvent
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /dom/TransitionEvent
standardization_status: 'W3C Working Draft'
summary: 'The amount of time the transition has been running, in seconds.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/TransitionEvent/elapsedTime

---
## Summary

The amount of time the transition has been running, in seconds.

Property of [dom/TransitionEvent](/dom/TransitionEvent)[dom/TransitionEvent](/dom/TransitionEvent)

## Syntax

**Note**: This property is read-only.

``` js
var result = object.elapsedTime;
```

## Return Value

Returns an object of type NumberNumber

Type: Floating-point

The amount of time the transition has been running, in seconds, when this event fired.

## Examples

MSDN hands-on CSS3 Animations wizard.

``` html

```

[View live example](http://ie.microsoft.com/testdrive/Graphics/hands-on-css3/hands-on_animations.htm)

## Notes

### Remarks

**Note**  This value is not affected by the value of [**transition-delay**](/css/properties/transition-delay).

### Syntax
