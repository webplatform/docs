---
title: clone
attributions:
  - 'Portions of this content come from HTML5Rocks! [article](http://updates.html5rocks.com/2014/05/Web-Animations---element-animate-is-now-in-Chrome-36)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: 'apis/web animations/Animation'
    href: /apis/web_animations/Animation
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/web_animations/Animation
standardization_status: 'W3C Working Draft'
summary: 'Creates a copy of an Animation object.'
tags:
  - API
  - Object
  - Methods
  - Web
  - Animations
uri: 'apis/web animations/Animation/clone'

---
## <span>Summary</span>

Creates a copy of an Animation object.

Method of [apis/web animations/Animation](/apis/web_animations/Animation)[apis/web animations/Animation](/apis/web_animations/Animation)

## <span>Syntax</span>

``` js
var myMiniMe = myAnimation.clone();
```

## <span>Return Value</span>

Returns an object of type<span></span>

Return a new Animation object created by calling the Animation constructor with parameters Animation(source.target, cloned effect, cloned timing).

## <span>Examples</span>

This example creates an instance of the AnimationPlayer that animates an object horizontally and vertically using computed values, and runs for 1500ms (1.5 seconds), and then creates a copy of the player for later use.

``` js
var player = snowFlake.animate([
  {transform: 'translate(' + snowLeft + 'px, -100%)'},
  {transform: 'translate(' + snowLeft + 'px, ' + window.innerHeight + 'px)'}
], 1500);
var player2 = player.clone();
```

## <span>Related specifications</span>

[Web Animations 1.0](http://www.w3.org/TR/web-animations/)
:   W3C Working Draft
