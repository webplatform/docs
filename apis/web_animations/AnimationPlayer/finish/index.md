---
title: finish
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: 'apis/web animations/AnimationPlayer'
    href: /apis/web_animations/AnimationPlayer
standardization_status: 'W3C Editor''s Draft'
summary: 'Seeks the player to the end of the source content in the current direction by running the finish a player procedure for this object.'
tags:
  - API
  - Object
  - Methods
  - Web
  - Animations
uri: 'apis/web animations/AnimationPlayer/finish'

---
## <span>Summary</span>

Seeks the player to the end of the source content in the current direction by running the finish a player procedure for this object.

Method of [apis/web animations/AnimationPlayer](/apis/web_animations/AnimationPlayer)[apis/web animations/AnimationPlayer](/apis/web_animations/AnimationPlayer)

## <span>Syntax</span>

``` js
 AnimationPlayer.finish();
```

## <span>Return Value</span>

No return value

**Needs Examples**: This section should include examples.

## <span>Usage</span>

     Exceptions:

DOMException of type InvalidStateError Raised if the end time of this player’s source content is infinity and the player playback rate is \> zero.