---
title: playState
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/web_animations/AnimationPlayer
    href: /apis/web_animations/AnimationPlayer
  return:
    predicate: 'Returns an object of type '
    value: enum
    href: /apis/web_animations/AnimationPlayer
standardization_status: 'W3C Editor''s Draft'
summary: 'The play state of this player.'
tags:
  - API
  - Object
  - Properties
  - Web
  - Animations
uri: 'apis/web animations/AnimationPlayer/playState'

---
## Summary

The play state of this player.

Property of [apis/web\_animations/AnimationPlayer](/apis/web_animations/AnimationPlayer)[apis/web\_animations/AnimationPlayer](/apis/web_animations/AnimationPlayer)

## Syntax

**Note**: This property is read-only.

``` js
var currentState = myPlayer.playState;
```

## Return Value

Returns an object of type enumenum

Returns a value from the AnimationPlayState enumeration.

enum AnimationPlayState { "idle", "pending", "running", "paused", "finished" }; idle Corresponds to the idle play state. pending Corresponds to the pending play state. running Corresponds to the running play state. paused Corresponds to the paused play state. finished Corresponds to the finished play state. 5.4

**Needs Examples**: This section should include examples.

