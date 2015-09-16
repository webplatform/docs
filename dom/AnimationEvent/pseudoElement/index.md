---
title: 'pseudoElement'
notes:
  - 'Needs spec reference, standardization status'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/AnimationEvent
    href: /dom/AnimationEvent
summary: 'A DOMString, starting with &quot;::&quot;, containing the name of the pseudo-element the animation runs on. If the animation runs on the element rather than on a pseudo-element, this property contains an empty string, &quot;&quot;.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/AnimationEvent/pseudoElement

---
## Summary

A DOMString, starting with &quot;::&quot;, containing the name of the pseudo-element the animation runs on. If the animation runs on the element rather than on a pseudo-element, this property contains an empty string, &quot;&quot;.

Property of [dom/AnimationEvent](/dom/AnimationEvent)[dom/AnimationEvent](/dom/AnimationEvent)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.pseudoElement;
```

## Examples

``` js
//for a predefined animation event
var myAnimEvent = new AnimationEvent();
// . . .
//retrieve the pseudo-element if used
var myAnimPseudoElem = myAnimEvent.pseudoElement;
```

