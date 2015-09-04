---
title: KeyframeEffect
tags:
  - API
  - Objects
  - Web
  - Animations
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
summary: 'Keyframe animation effects are represented by the KeyframeEffect interface.'
uri: 'apis/web animations/KeyframeEffect'

---
# KeyframeEffect

## Summary

Keyframe animation effects are represented by the KeyframeEffect interface.

<span data-meta="subclass_of" data-type="key">Inherits from <span data-type="value">[AnimationEffect](/apis/web_animations/AnimationEffect)</span></span>

## Properties

API Name
:   Summary
[spacing](/apis/web_animations/KeyframeEffect/spacing)
:   The spacing mode to use for this animation effect.

## Methods

API Name
:   Summary
[constructor](/apis/web_animations/KeyframeEffect/constructor)
:   Creates a new KeyframeEffect object for the given set of keyframes.
[getFrames](/apis/web_animations/KeyframeEffect/getFrames)
:   Returns the keyframes that make up this effect as a sequence of ComputedKeyframe objects.
[setFrames](/apis/web_animations/KeyframeEffect/setFrames)
:   A Keyframe object or sequence of Keyframe objects used to replace the set of keyframes that make up this effect.

## Events

*No events.*

## Inherited from AnimationEffect

### Properties

API Name
:   Summary
[composite](/apis/web_animations/AnimationEffect/composite)
:   The possible values of an animation effect's composition behavior are represented by the CompositeOperation enumeration.
[iterationComposite](/apis/web_animations/AnimationEffect/iterationComposite)
:   The iteration composite operation property of this animation effect as specified by one of the IterationCompositeOperation enumeration values.
[name](/apis/web_animations/AnimationEffect/name)
:   A string used to identify the effect.

### Methods

API Name
:   Summary
[clone](/apis/web_animations/AnimationEffect/clone)
:   Creates and returns a new object of the same type as this object's most-derived interface such that it will produce the same output as this object.

### Events

*No events.*

**Needs Examples**: This section should include examples.

