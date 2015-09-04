---
title: playState
tags:
  - API
  - Object
  - Properties
  - Web
  - Animations
readiness: 'Almost Ready'
standardization_status: 'W3C Editor''s Draft'
summary: 'The play state of this player.'
uri: 'apis/web animations/AnimationPlayer/playState'

---
# playState

## Summary

The play state of this player.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/web\_animations/AnimationPlayer](/apis/web_animations/AnimationPlayer)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var currentState = myPlayer.playState;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">enum</span></span>

Returns a value from the AnimationPlayState enumeration.

enum AnimationPlayState { "idle", "pending", "running", "paused", "finished" }; idle Corresponds to the idle play state. pending Corresponds to the pending play state. running Corresponds to the running play state. paused Corresponds to the paused play state. finished Corresponds to the finished play state. 5.4

**Needs Examples**: This section should include examples.

