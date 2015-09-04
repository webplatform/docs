---
title: pseudoElement
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
notes:
  - 'Needs spec reference, standardization status'
summary: 'A DOMString, starting with "::", containing the name of the pseudo-element the animation runs on. If the animation runs on the element rather than on a pseudo-element, this property contains an empty string, "".'
uri: dom/AnimationEvent/pseudoElement

---
# pseudoElement

## Summary

A DOMString, starting with "::", containing the name of the pseudo-element the animation runs on. If the animation runs on the element rather than on a pseudo-element, this property contains an empty string, "".

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/AnimationEvent](/dom/AnimationEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.pseudoElement;
```

## Examples

``` {.js}
//for a predefined animation event
var myAnimEvent = new AnimationEvent();
// . . .
//retrieve the pseudo-element if used
var myAnimPseudoElem = myAnimEvent.pseudoElement;
```

