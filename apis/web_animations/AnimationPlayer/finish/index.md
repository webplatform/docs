---
title: finish
tags:
  - API
  - Object
  - Methods
  - Web
  - Animations
readiness: 'Almost Ready'
standardization_status: 'W3C Editor''s Draft'
summary: 'Seeks the player to the end of the source content in the current direction by running the finish a player procedure for this object.'
uri: 'apis/web animations/AnimationPlayer/finish'

---
# finish

## Summary

Seeks the player to the end of the source content in the current direction by running the finish a player procedure for this object.

*Method of [apis/web animations/AnimationPlayer](/apis/web_animations/AnimationPlayer)*

## Syntax

``` {.js}
 AnimationPlayer.finish();
```

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Usage

     Exceptions:

DOMException of type InvalidStateError Raised if the end time of this player’s source content is infinity and the player playback rate is \> zero.

