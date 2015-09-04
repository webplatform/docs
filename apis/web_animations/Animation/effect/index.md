---
title: effect
tags:
  - API
  - Object
  - Properties
  - Web
  - Animations
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
uri: 'apis/web animations/Animation/effect'

---
# effect

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/web\_animations/Animation](/apis/web_animations/Animation)</span></span>

## Syntax

``` {.js}
var myEffect = myAnimation.effect;
myAnimation.effect = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value"></span></span>

The effect parameter, an ECMAScript value passed to the Animation constructor or to the animate operation of the Animatable interface, may specify an EffectCallback, an AnimationEffect, a Keyframe a sequence of Keyframes, or null. However, since callback functions and dictionaries are not distinguishable in WebIDL, we define the processing of this parameter for ECMAScript here in prose.

The procedure for converting an effect to an IDL value with parameter effect is as follows:

If effect is null, Return null. If effect is a platform object that implements AnimationEffect, return the IDL value that is a reference to the that platform object. If IsCallable(effect) is true, Return the result of applying the procedure for converting an ECMAScript value to an IDL callback function type to effect using EffectCallback as the callback function type. Otherwise, Return a new KeyframeEffect object constructed passing effect as the frames parameter.

**Needs Examples**: This section should include examples.

