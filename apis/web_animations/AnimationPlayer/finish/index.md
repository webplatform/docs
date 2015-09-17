---
title: 'finish'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: 'apis/web animations/AnimationPlayer'
    href: /apis/web_animations/AnimationPlayer
standardization_status: 'W3C Editor''s Draft'
summary: 'Seeks the player to the end of the source content in the current direction by running the finish a player procedure for this object.'
tags:
  - API_Object_Methods
  - Web_Animations
  - Needs_Examples
uri: 'apis/web animations/AnimationPlayer/finish'

---
## Summary

Seeks the player to the end of the source content in the current direction by running the finish a player procedure for this object.

Method of [apis/web animations/AnimationPlayer](/apis/web_animations/AnimationPlayer)[apis/web animations/AnimationPlayer](/apis/web_animations/AnimationPlayer)

## Syntax

``` js
 AnimationPlayer.finish();
```

## Return Value

No return value

## Usage

     Exceptions:

DOMException of type InvalidStateError Raised if the end time of this player’s source content is infinity and the player playback rate is \> zero.
