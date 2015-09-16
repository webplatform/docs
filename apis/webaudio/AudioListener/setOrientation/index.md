---
title: 'setOrientation'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/webaudio/AudioListener
    href: /apis/webaudio/AudioListener
  return_type:
    predicate: 'Returns an object of type  '
    value: Number
    href: /apis/webaudio/AudioListener
standardization_status: 'W3C Editor''s Draft'
summary: 'Describes which direction the listener is pointing in the 3D cartesian coordinate space. Both a front vector and an up vector are provided. In human terms, the front vector represents which direction the person''s nose is pointing. The up vector represents the direction the top of a person''s head is pointing. These values are expected to be linearly independent (at right angles to each other). The x, y, z parameters represent a front direction vector in 3D space, with the default value being (0,0,-1). The xUp, yUp, zUp parameters represent an up direction vector in 3D space, with the default value being (0,1,0).'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AudioListener/setOrientation

---
## Summary

Describes which direction the listener is pointing in the 3D cartesian coordinate space. Both a front vector and an up vector are provided. In human terms, the front vector represents which direction the person's nose is pointing. The up vector represents the direction the top of a person's head is pointing. These values are expected to be linearly independent (at right angles to each other). The x, y, z parameters represent a front direction vector in 3D space, with the default value being (0,0,-1). The xUp, yUp, zUp parameters represent an up direction vector in 3D space, with the default value being (0,1,0).

Method of [apis/webaudio/AudioListener](/apis/webaudio/AudioListener)[apis/webaudio/AudioListener](/apis/webaudio/AudioListener)

## Syntax

``` js
var  = AudioListener.setOrientation(x, y, z, xUp, yUp, zUp);
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

### xUp

 Data-type
:   Number

### yUp

 Data-type
:   Number

### zUp

 Data-type
:   Number

## Return Value

Returns an object of type NumberNumber

## Examples

``` js
var audioCtx = new AudioContext();
var myListener = audioCtx.listener;
myListener.setOrientation(0,0,-1,0,1,0);
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
