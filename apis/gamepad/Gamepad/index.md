---
title: Gamepad
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'This object defines an individual gamepad device. Data is retrieved via the DOM Navigator object''s getGamepads() method.'
tags:
  0: API
  1: Objects
  3: Gamepad
uri: apis/gamepad/Gamepad

---
## Summary

This object defines an individual gamepad device. Data is retrieved via the DOM Navigator object's getGamepads() method.

## Properties

API Name
:   Summary

[axes](/apis/gamepad/Gamepad/axes)
:   Array of values for all axes of the gamepad. Each entry in the array is a floating point value in the range -1.0 - 1.0, representing the axis position from the lowest value (-1.0) to the highest value (1.0).

[buttons](/apis/gamepad/Gamepad/buttons)
:   Array of values for all buttons of the gamepad.

[id](/apis/gamepad/Gamepad/id)
:   A string that identifies the brand or style of connected gamepad device.

[index](/apis/gamepad/Gamepad/index)
:   The index of the gamepad in the **Navigator**.

[timestamp](/apis/gamepad/Gamepad/timestamp)
:   A timestamp indicating the last time the data for this gamepad was updated.

## Methods

*No methods.*

## Events

*No events.*

## Related specifications

[W3C Gamepad Specification](https://dvcs.w3.org/hg/gamepad/raw-file/default/gamepad.html)
:   W3C Working Draft
