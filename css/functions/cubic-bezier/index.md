---
title: 'cubic-bezier'
code_samples:
  - 'http://letmespellitoutforyou.com/samples/transit_timing.html'
compatibility:
  feature: cubic-bezier
  topic: css
readiness: 'Ready to Use'
summary: 'An animation timing function that describes a progression of movement as a cubic-bezier curve.'
tags:
  - CSS
  - Functions
uri: css/functions/cubic-bezier

---
## Summary

An animation timing function that describes a progression of movement as a cubic-bezier curve.

 The function describes a cubic bezier curve starting at 0,0 and ending at 1,1. It accepts four arguments (x1, y1, x2, y2) that specify coordinates for the two control points that affect the shape of the curve. The following shows standard timing keyword values along with their functional equivalents. The *x* axis represents the elapsed time of the animation, and *y* represents the progression of movement, so the more the curve points upwards, the faster the animation moves at that point:

**linear**
**cubic-bezier(0.0, 0.0, 1.0, 1.0)** ![transitF linear.png](/assets/thumb/8/8e/transitF_linear.png/230px-transitF_linear.png)

**ease**
**cubic-bezier(0.25, 0.1, 0.25, 1.0)** ![transitF ease.png](/assets/thumb/7/73/transitF_ease.png/230px-transitF_ease.png)

**ease-in-out**
**cubic-bezier(0.42, 0, 0.58, 1.0)** ![transitF easeinout.png](/assets/thumb/6/67/transitF_easeinout.png/230px-transitF_easeinout.png)

**ease-in**
**cubic-bezier(0.42, 0, 1.0, 1.0)** ![transitF easein.png](/assets/thumb/6/64/transitF_easein.png/230px-transitF_easein.png)

**ease-out**
**cubic-bezier(0, 0, 0.58, 1.0)** ![transitF easeout.png](/assets/thumb/0/00/transitF_easeout.png/230px-transitF_easeout.png)

For properties unrelated to opacity and color, the function accepts *y* coordinates outside the standard range between 0 and 1. This allows for "elastic" effects in which positions or dimensions may cross over themselves during the course of the progression. The first example below bounces past its start and end points, while the second oscillates more dramatically:

**cubic-bezier(0.25, -0.5, 0.75, 1.5)** ![transitF cubicBounce.png](/assets/thumb/2/2d/transitF_cubicBounce.png/230px-transitF_cubicBounce.png)

**cubic-bezier(0.5, 2, 0.5, -1)** ![transitF cubicWave.png](/assets/thumb/2/2d/transitF_cubicWave.png/230px-transitF_cubicWave.png)

## Examples

A dramatically oscillating timing function whose *y* values lie far outside the 0-1 range:

``` css
transition-timing-function: cubic-bezier(0.5,3.0,0.5,-2.0);
```

Modify the timing function for a sequence of two transitions

```

```

[View live example](http://letmespellitoutforyou.com/samples/transit_timing.html)

## See also

### Related articles

#### Animation

-   [Web Animations API](/apis/web_animations)

-   [clone](/apis/web_animations/AnimationEffect/clone)

-   [AnimationNode](/apis/web_animations/AnimationNode)

-   [timing](/apis/web_animations/AnimationNode/timing)

-   [currentTime](/apis/web_animations/AnimationPlayer/currentTime)

-   [reverse](/apis/web_animations/AnimationPlayer/reverse)

-   [source](/apis/web_animations/AnimationPlayer/source)

-   [AnimationPlayerEvent](/apis/web_animations/AnimationPlayerEvent)

-   [currentTime](/apis/web_animations/AnimationTimeline/currentTime)

-   [play](/apis/web_animations/AnimationTimeline/play)

-   [@keyframes](/css/atrules/@keyframes)

-   [CSSKeyframeRule](/css/cssom/CSSKeyframeRule)

-   [keyText](/css/cssom/CSSKeyframeRule/keyText)

-   [style](/css/cssom/CSSKeyframeRule/style)

-   [CSSKeyframesRule](/css/cssom/CSSKeyframesRule)

-   [cssRules](/css/cssom/CSSKeyframesRule/cssRules)

-   [deleteRule](/css/cssom/CSSKeyframesRule/deleteRule)

-   [findRule](/css/cssom/CSSKeyframesRule/findRule)

-   [insertRule](/css/cssom/CSSKeyframesRule/insertRule)

-   [name](/css/cssom/CSSKeyframesRule/name)

-   **cubic-bezier**

-   [Animations](/css/properties/animations)

-   [transition](/css/properties/transition)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

#### Transitions

-   **cubic-bezier**

-   [transition](/css/properties/transition)

-   [transition-delay](/css/properties/transition-delay)

-   [transition-duration](/css/properties/transition-duration)

-   [transition-property](/css/properties/transition-property)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)
