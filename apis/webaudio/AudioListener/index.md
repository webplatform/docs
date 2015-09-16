---
title: AudioListener
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'This interface represents the position and orientation of the person listening to the audio scene. All PannerNode objects spatialize in relation to the AudioContext''s listener.'
tags:
  0: API
  1: Objects
  3: WebAudio
uri: apis/webaudio/AudioListener

---
## Summary

This interface represents the position and orientation of the person listening to the audio scene. All PannerNode objects spatialize in relation to the AudioContext's listener.

## Properties

API Name
:   Summary

[dopplerFactor](/apis/webaudio/AudioListener/dopplerFactor)
:   A constant used to determine the amount of pitch shift to use when rendering a doppler effect. The default value is 1.

[speedOfSound](/apis/webaudio/AudioListener/speedOfSound)
:   The speed of sound used for calculating doppler shift. The default value is 343.3 meters / second.

## Methods

API Name
:   Summary

[setOrientation](/apis/webaudio/AudioListener/setOrientation)
:   Describes which direction the listener is pointing in the 3D cartesian coordinate space. Both a front vector and an up vector are provided. In human terms, the front vector represents which direction the person's nose is pointing. The up vector represents the direction the top of a person's head is pointing. These values are expected to be linearly independent (at right angles to each other). The x, y, z parameters represent a front direction vector in 3D space, with the default value being (0,0,-1). The xUp, yUp, zUp parameters represent an up direction vector in 3D space, with the default value being (0,1,0).

[setPosition](/apis/webaudio/AudioListener/setPosition)
:   Sets the position of the listener in a 3D cartesian coordinate space. [**PannerNode**](/apis/webaudio/PannerNode) objects use this position relative to individual audio sources for spatialization. The x, y, z parameters represent the coordinates in 3D space. The default value is (0,0,0).

[setVelocity](/apis/webaudio/AudioListener/setVelocity)
:   Sets the velocity vector of the listener. This vector controls both the direction of travel and the speed in 3D space. This velocity relative an audio source's velocity is used to determine how much doppler shift (pitch change) to apply. The x, y, z parameters describe a direction vector indicating direction of travel and intensity. The default value is (0,0,0).

## Events

*No events.*

## Related specifications

[W3C Web Audio API](https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html)
:   W3C Editor's Draft
