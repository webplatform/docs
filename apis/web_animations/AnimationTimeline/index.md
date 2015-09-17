---
title: 'AnimationTimeline'
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
summary: 'Representation of a timeline, including the document timeline.'
tags:
  - API_Objects
  - API
  - Web_Animations
  - Needs_Examples
uri: 'apis/web animations/AnimationTimeline'

---
## Summary

Representation of a timeline, including the document timeline.

## Properties

[currentTime](/apis/web_animations/AnimationTimeline/currentTime)
:   Returns the time value for this timeline or null if this timeline is inactive.

## Methods

[getAnimationPlayers](/apis/web_animations/AnimationTimeline/getAnimationPlayers)
:   Returns the set of [**Animation Player**](/apis/web_animations/AnimationPlayer) objects associated with this timeline that have associated source content which is current or in effect.

[play](/apis/web_animations/AnimationTimeline/play)
:   Creates a new [**AnimationPlayer**](/apis/web_animations/AnimationPlayer) object associated with this timeline that begins playback as soon as it is ready.

## Events

*No events.*
