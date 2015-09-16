---
title: animate
attributions:
  - 'Portions of this content come from HTML5Rocks! [article](http://updates.html5rocks.com/2014/05/Web-Animations---element-animate-is-now-in-Chrome-36)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/web_animations/Animatable
    href: /apis/web_animations/Animatable
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/web_animations/Animatable
standardization_status: 'W3C Working Draft'
summary: 'Creates a new Animation object whose animation target is the object on which the method is called, and calls the play method of the AnimationTimeline object of the document timeline of the node document [DOM4] of the element, passing the newly created Animation as the argument to the method.'
tags:
  - API
  - Object
  - Methods
  - Web
  - Animations
uri: 'apis/web animations/Animatable/animate'

---
## Summary

Creates a new Animation object whose animation target is the object on which the method is called, and calls the play method of the AnimationTimeline object of the document timeline of the node document [DOM4] of the element, passing the newly created Animation as the argument to the method.

Method of [apis/web\_animations/Animatable](/apis/web_animations/Animatable)[apis/web\_animations/Animatable](/apis/web_animations/Animatable)

## Syntax

``` js
var myAnimationPlayer = myAnimationPlayer.animate();
```

## Return Value

Returns an object of type

Returns the AnimationPlayer object returned by the play method of the AnimationTimeline.

## Examples

This example creates an instance of the AnimationPlayer that animates an object horizontally and vertically using computed values, and runs for 1500ms (1.5 seconds).

``` js
var player = snowFlake.animate([
  {transform: 'translate(' + snowLeft + 'px, -100%)'},
  {transform: 'translate(' + snowLeft + 'px, ' + window.innerHeight + 'px)'}
], 1500);
```

## Related specifications

[Web Animations 1.0](http://www.w3.org/TR/web-animations/)
:   W3C Working Draft
