---
title: PannerNode
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'This interface represents a processing node which positions / spatializes an incoming audio stream in three-dimensional space. The spatialization is in relation to the AudioContext''s AudioListener (listener attribute). The audio stream from the input will be either mono or stereo, depending on the connection(s) to the input. The output of this node is hard-coded to stereo (2 channels) and currently cannot be configured.'
tags:
  0: API
  1: Objects
  3: WebAudio
uri: apis/webaudio/PannerNode

---
## Summary

This interface represents a processing node which positions / spatializes an incoming audio stream in three-dimensional space. The spatialization is in relation to the AudioContext's AudioListener (listener attribute). The audio stream from the input will be either mono or stereo, depending on the connection(s) to the input. The output of this node is hard-coded to stereo (2 channels) and currently cannot be configured.

## Properties

API Name
:   Summary

[coneInnerAngle](/apis/webaudio/PannerNode/coneInnerAngle)
:   A parameter for directional audio sources, this is an angle inside of which there will be no volume reduction. The default value is 360.

[coneOuterAngle](/apis/webaudio/PannerNode/coneOuterAngle)
:   A parameter for directional audio sources, this is an angle outside of which the volume will be reduced to a constant value of [**coneOuterGain**](/apis/webaudio/PannerNode/coneOuterGain). The default value is 360.

[coneOuterGain](/apis/webaudio/PannerNode/coneOuterGain)
:   A parameter for directional audio sources, this is the amount of volume reduction outside of the [**coneOuterAngle**](/apis/webaudio/PannerNode/coneOuterAngle). The default value is 0.

[distanceModel](/apis/webaudio/PannerNode/distanceModel)
:   Determines which algorithm will be used to reduce the volume of an audio source as it moves away from the listener. See below for the available choices. The default is INVERSE\_DISTANCE.

[maxDistance](/apis/webaudio/PannerNode/maxDistance)
:   The maximum distance between source and listener, after which the volume will not be reduced any further. The default value is 10000.

[panningModel](/apis/webaudio/PannerNode/panningModel)
:   Determines which spatialization algorithm will be used to position the audio in 3D space. See below for the available choices. The default is HRTF.

[refDistance](/apis/webaudio/PannerNode/refDistance)
:   A reference distance for reducing volume as source moves further from the listener. The default value is 1.

[rolloffFactor](/apis/webaudio/PannerNode/rolloffFactor)
:   Describes how quickly the volume is reduced as source moves away from listener. The default value is 1.

## Methods

API Name
:   Summary

[setOrientation](/apis/webaudio/PannerNode/setOrientation)
:   Describes which direction the audio source is pointing in the 3D cartesian coordinate space. Depending on how directional the sound is (controlled by the cone attributes), a sound pointing away from the listener can be very quiet or completely silent. The x, y, and z parameters represent a direction vector in 3D space. The default value is (1,0,0).

[setPosition](/apis/webaudio/PannerNode/setPosition)
:   Sets the position of the audio source relative to the listener attribute. A 3D cartesian coordinate system is used. The x, y, and z parameters represent the coordinates in 3D space. The default value is (0,0,0).

[setVelocity](/apis/webaudio/PannerNode/setVelocity)
:   Sets the velocity vector of the audio source. This vector controls both the direction of travel and the speed in 3D space. This velocity relative to the listener's velocity is used to determine how much doppler shift (pitch change) to apply. The x, y, and z parameters describe a direction vector indicating direction of travel and intensity. The default value is (0,0,0).

## Events

*No events.*

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
