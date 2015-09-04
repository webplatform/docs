---
title: getFrames
tags:
  - API
  - Object
  - Methods
  - Web
  - Animations
readiness: 'Almost Ready'
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns the keyframes that make up this effect as a sequence of ComputedKeyframe objects.'
uri: 'apis/web animations/KeyframeEffect/getFrames'

---
# getFrames

## Summary

Returns the keyframes that make up this effect as a sequence of ComputedKeyframe objects.

*Method of [apis/web\_animations/KeyframeEffect](/apis/web_animations/KeyframeEffect)*

## Syntax

``` {.js}
var  = .getFrames();
```

## Return Value

Returns an object of type Object.

Returns a sequence of ComputedKeyFrame objects.

The value returned differs from the frames parameter passed into setFrames or the constructor for this interface in the following ways:

The normalization defined in §5.17.3 Normalizing a sequence of keyframes is applied to frames which may result in some frames being removed or re-ordered and some properties being removed. This normalization will also cause a single Keyframe object to be replaced with a sequence. The result of computing the keyframe offset of each keyframe as defined in §4.3.1 Spacing keyframes is stored in the computedOffset member of each frame.

**Needs Examples**: This section should include examples.

