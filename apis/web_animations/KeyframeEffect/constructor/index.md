---
title: 'constructor'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/web_animations/KeyframeEffect
    href: /apis/web_animations/KeyframeEffect
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/web_animations/KeyframeEffect
standardization_status: 'W3C Editor''s Draft'
summary: 'Creates a new KeyframeEffect object for the given set of keyframes.'
tags:
  - API_Object_Methods
  - Web_Animations
  - Needs_Examples
uri: 'apis/web animations/KeyframeEffect/constructor'

---
## Summary

Creates a new KeyframeEffect object for the given set of keyframes.

Method of [apis/web\_animations/KeyframeEffect](/apis/web_animations/KeyframeEffect)[apis/web\_animations/KeyframeEffect](/apis/web_animations/KeyframeEffect)

## Syntax

``` js
var  = .constructor(frames, KeyframeEffectOptions, options);
```

## Parameters

### frames, KeyframeEffectOptions

 Data-type
:   Object

 A Keyframe object or sequence of Keyframe objects used for calculating animation values for this animation effect. The constraints on this parameter and its processing are identical to those for setFrames.

### options

 Data-type
:   String

(Optional)

A KeyframeEffectOptions dictionary defining other aspects of the animation effect’s behavior. If this parameter is not provided, the default values of the dictionary are used.

## Return Value

Returns an object of type
