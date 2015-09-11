---
title: AudioParam
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'AudioParam controls an individual aspect of an AudioNode''s functioning, such as volume. The parameter can be set immediately to a particular value using the value attribute. Or, value changes can be scheduled to happen at very precise times (in the coordinate system of AudioContext.currentTime), for envelopes, volume fades, LFOs, filter sweeps, grain windows, etc. In this way, arbitrary timeline-based automation curves can be set on any AudioParam. Additionally, audio signals from the outputs of AudioNodes can be connected to an AudioParam, summing with the intrinsic parameter value.'
tags:
  0: API
  1: Objects
  3: WebAudio
uri: apis/webaudio/AudioParam

---
## <span>Summary</span>

AudioParam controls an individual aspect of an AudioNode's functioning, such as volume. The parameter can be set immediately to a particular value using the value attribute. Or, value changes can be scheduled to happen at very precise times (in the coordinate system of AudioContext.currentTime), for envelopes, volume fades, LFOs, filter sweeps, grain windows, etc. In this way, arbitrary timeline-based automation curves can be set on any AudioParam. Additionally, audio signals from the outputs of AudioNodes can be connected to an AudioParam, summing with the intrinsic parameter value.

## <span>Properties</span>

API Name
:   Summary

[computedValue](/apis/webaudio/AudioParam/computedValue)
:   The final value controlling the audio DSP, calculated at each time, which is either the value set directly to the value attribute or, if there are any scheduled parameter changes (automation events), the value as calculated from these events.

    **Not in spec; deletion candidate. See <http://webaudio.github.io/web-audio-api/>.**

[defaultValue](/apis/webaudio/AudioParam/defaultValue)
:   Initial value for the value attribute.

[maxValue](/apis/webaudio/AudioParam/maxValue)
:   Nominal maximum value. The value attribute may be set higher than this value.

    **Not in spec; deletion candidate. See <http://webaudio.github.io/web-audio-api/>.**

[minValue](/apis/webaudio/AudioParam/minValue)
:   Nominal minimum value. The value attribute may be set lower than this value.

    **Not in spec; deletion candidate. See <http://webaudio.github.io/web-audio-api/>.**

[value](/apis/webaudio/AudioParam/value)
:   The parameter's floating-point value. If a value is set outside the allowable range no exception is thrown, because these limits are nominal and may be exceeded. If a value is set during a time when there are any automation events scheduled then it will be ignored and no exception will be thrown.

## <span>Methods</span>

API Name
:   Summary

[cancelScheduledValues](/apis/webaudio/AudioParam/cancelScheduledValues)
:   Cancels all scheduled parameter changes with times greater than or equal to **startTime**.

[exponentialRampToValueAtTime](/apis/webaudio/AudioParam/exponentialRampToValueAtTime)
:   Schedules an exponential continuous change in parameter value from the previous scheduled parameter value to the given value. Parameters representing filter frequencies and playback rate are best changed exponentially because of the way humans perceive sound.

[linearRampToValueAtTime](/apis/webaudio/AudioParam/linearRampToValueAtTime)
:   Schedules a linear continuous change in parameter value from the previous scheduled parameter value to the given value.

[setTargetAtTime](/apis/webaudio/AudioParam/setTargetAtTime)
:   Start exponentially approaching the target value at the given time with a rate having the given time constant. Among other uses, this is useful for implementing the *decay* and *release* portions of an ADSR envelope. Please note that the parameter value does not immediately change to the target value at the given time, but instead gradually changes to the target value.

[setValueAtTime](/apis/webaudio/AudioParam/setValueAtTime)
:   Schedules a parameter value change at the given time.

[setValueCurveAtTime](/apis/webaudio/AudioParam/setValueCurveAtTime)
:   Sets an array of arbitrary parameter values starting at the given time for the given duration. The number of values will be scaled to fit into the desired duration.

## <span>Events</span>

*No events.*

## <span>Related specifications</span>

[W3C Web Audio API](https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html)
:   W3C Editor's Draft
