---
title: 'effect'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/web_animations/Animation
    href: /apis/web_animations/Animation
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /apis/web_animations/Animation
standardization_status: 'W3C Editor''s Draft'
tags:
  - API_Object_Properties
  - Web_Animations
  - Needs_Summary
  - Needs_Examples
uri: 'apis/web animations/Animation/effect'

---
Property of [apis/web\_animations/Animation](/apis/web_animations/Animation)[apis/web\_animations/Animation](/apis/web_animations/Animation)

## Syntax

``` js
var myEffect = myAnimation.effect;
myAnimation.effect = value;
```

## Return Value

Returns an object of type

The effect parameter, an ECMAScript value passed to the Animation constructor or to the animate operation of the Animatable interface, may specify an EffectCallback, an AnimationEffect, a Keyframe a sequence of Keyframes, or null. However, since callback functions and dictionaries are not distinguishable in WebIDL, we define the processing of this parameter for ECMAScript here in prose.

The procedure for converting an effect to an IDL value with parameter effect is as follows:

If effect is null, Return null. If effect is a platform object that implements AnimationEffect, return the IDL value that is a reference to the that platform object. If IsCallable(effect) is true, Return the result of applying the procedure for converting an ECMAScript value to an IDL callback function type to effect using EffectCallback as the callback function type. Otherwise, Return a new KeyframeEffect object constructed passing effect as the frames parameter.

