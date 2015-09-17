---
title: 'setOrientation'
notes:
  - Needsexample
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/webaudio/PannerNode
    href: /apis/webaudio/PannerNode
  return_type:
    predicate: 'Returns an object of type  '
    value: Number
    href: /apis/webaudio/PannerNode
standardization_status: 'W3C Editor''s Draft'
summary: 'Describes which direction the audio source is pointing in the 3D cartesian coordinate space. Depending on how directional the sound is (controlled by the cone attributes), a sound pointing away from the listener can be very quiet or completely silent. The x, y, and z parameters represent a direction vector in 3D space. The default value is (1,0,0).'
tags:
  - API_Object_Methods
  - API
  - WebAudio
uri: apis/webaudio/PannerNode/setOrientation

---
## Summary

Describes which direction the audio source is pointing in the 3D cartesian coordinate space. Depending on how directional the sound is (controlled by the cone attributes), a sound pointing away from the listener can be very quiet or completely silent. The x, y, and z parameters represent a direction vector in 3D space. The default value is (1,0,0).

Method of [apis/webaudio/PannerNode](/apis/webaudio/PannerNode)[apis/webaudio/PannerNode](/apis/webaudio/PannerNode)

## Syntax

``` js
var  = PannerNode.setOrientation(x, y, z);
```

## Parameters

### x

 Data-type
:   Number

### y

 Data-type
:   Number

### z

 Data-type
:   Number

## Return Value

Returns an object of type NumberNumber

## Examples

``` js
var audioCtx = new AudioContext();
var panner = audioCtx.createPanner();
panner.setOrientation(1,0,0);
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
