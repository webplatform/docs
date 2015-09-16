---
title: Animatable
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Objects that may be the target of an Animation implement the Animatable interface.'
tags:
  - API
  - Objects
  - Web
  - Animations
uri: 'apis/web animations/Animatable'

---
## Summary

Objects that may be the target of an Animation implement the Animatable interface.

## Properties

*No properties.*

## Methods

API Name
:   Summary

[animate](/apis/web_animations/Animatable/animate)
:   Creates a new Animation object whose animation target is the object on which the method is called, and calls the play method of the AnimationTimeline object of the document timeline of the node document [DOM4] of the element, passing the newly created Animation as the argument to the method.

## Events

*No events.*

## Examples

``` js
elem.ownerDocument.timeline.play(anim);
```

``` js
var anim = new Animation(elem, { opacity: 0 }, 2000);
```

``` js
var anim = elem.animate({ opacity: 0 }, 2000);
```

## Related specifications

[Web Animations 1.0](http://www.w3.org/TR/web-animations/)
:   W3C Working Draft
