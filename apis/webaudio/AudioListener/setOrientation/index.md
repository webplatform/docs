---
title: setOrientation
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Describes which direction the listener is pointing in the 3D cartesian coordinate space. Both a front vector and an up vector are provided. In human terms, the front vector represents which direction the person''s nose is pointing. The up vector represents the direction the top of a person''s head is pointing. These values are expected to be linearly independent (at right angles to each other). The x, y, z parameters represent a front direction vector in 3D space, with the default value being (0,0,-1). The xUp, yUp, zUp parameters represent an up direction vector in 3D space, with the default value being (0,1,0).'
uri: apis/webaudio/AudioListener/setOrientation

---
# setOrientation

## Summary

Describes which direction the listener is pointing in the 3D cartesian coordinate space. Both a front vector and an up vector are provided. In human terms, the front vector represents which direction the person's nose is pointing. The up vector represents the direction the top of a person's head is pointing. These values are expected to be linearly independent (at right angles to each other). The x, y, z parameters represent a front direction vector in 3D space, with the default value being (0,0,-1). The xUp, yUp, zUp parameters represent an up direction vector in 3D space, with the default value being (0,1,0).

*Method of [apis/webaudio/AudioListener](/apis/webaudio/AudioListener)*

## Syntax

``` {.js}
var  = AudioListener.setOrientation(x, y, z, xUp, yUp, zUp);
```

## Parameters

### x

 Data-typeÂ
:   Number

### y

 Data-typeÂ
:   Number

### z

 Data-typeÂ
:   Number

### xUp

 Data-typeÂ
:   Number

### yUp

 Data-typeÂ
:   Number

### zUp

 Data-typeÂ
:   Number

## Return Value

Returns an object of type Number.

## Examples

``` {.js}
var audioCtx = new AudioContext();
var myListener = audioCtx.listener;
myListener.setOrientation(0,0,-1,0,1,0);
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

