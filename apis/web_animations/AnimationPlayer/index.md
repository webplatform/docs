---
title: AnimationPlayer
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
summary: 'Represents a single animation player. Players connect animation node, or source, to a timeline and provides playback controls.'
tags:
  - API
  - Objects
  - Web
  - Animations
uri: 'apis/web animations/AnimationPlayer'

---
## Summary

Represents a single animation player. Players connect animation node, or source, to a timeline and provides playback controls.

## Properties

API Name
:   Summary

[currentTime](/apis/web_animations/AnimationPlayer/currentTime)
:   The current time of this player unless this player has a pending pause task, in which case this attribute returns null.

[finished](/apis/web_animations/AnimationPlayer/finished)
:   Returns the current finished promise for this object.

[playState](/apis/web_animations/AnimationPlayer/playState)
:   The play state of this player.

[playbackRate](/apis/web_animations/AnimationPlayer/playbackRate)
:   The playback rate of this player. Setting this attribute follows the procedure to update the player playback rate of this object to the new value.

[ready](/apis/web_animations/AnimationPlayer/ready)
:   Returns the current ready promise for this object.

[source](/apis/web_animations/AnimationPlayer/source)
:   The source content associated with this player. Setting this attribute updates the object’s source content using the procedure to set the source content of a player.

[startTime](/apis/web_animations/AnimationPlayer/startTime)
:   Returns the start time of this player. Setting this attribute updates the player start time using the procedure to update the player start time of this object to the new value.

[timeline](/apis/web_animations/AnimationPlayer/timeline)
:   The timeline associated with this player. Setting this attribute updates the object’s timeline using the procedure to set the timeline of a player.

## Methods

API Name
:   Summary

[cancel](/apis/web_animations/AnimationPlayer/cancel)
:   Clears all effects caused by this player and aborts its playback by running the cancel a player procedure for this object.

[constructor](/apis/web_animations/AnimationPlayer/constructor)
:   Constructs an new AnimationPlayer object.

[finish](/apis/web_animations/AnimationPlayer/finish)
:   Seeks the player to the end of the source content in the current direction by running the finish a player procedure for this object.

[pause](/apis/web_animations/AnimationPlayer/pause)
:   Suspends the playback of this player by running the procedure to pause a player for this object.

[play](/apis/web_animations/AnimationPlayer/play)
:   Unpauses the player and rewinds if it has finished playing using the procedure to play a player for this object.

[reverse](/apis/web_animations/AnimationPlayer/reverse)
:   Inverts the playback rate of this player and seeks to the start of the source content if if has finished playing in the reversed direction using the reverse a player procedure for this object.

## Events

*No events.*

**Needs Examples**: This section should include examples.

