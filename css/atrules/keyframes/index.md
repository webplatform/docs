---
title: @keyframes
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://03sq.net/examples/animation.html'
  - 'http://03sq.net/examples/animation2.html'
notes:
  - "Empty \"Main Content\" section, see @import for notes for improvement. \nIn the summary, \"Keyframes\" is defined using itself, would reword and provide a working definition of \"Keyframes\" to the general public."
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
summary: 'Sets the keyframes for the CSS animation property.'
tags:
  - CSS
  - At
  - Rules
uri: css/atrules/@keyframes

---
## Summary

Sets the keyframes for the CSS animation property.

## Examples

Example of prefixed/prefix-free @keyframes blocks

``` css
/* defining the animation */
@keyframes fadeInAnimation {
    /* starting state */
    from {
        opacity: 0;
    }
    /* ending state */
    to {
        opacity: 1;
    }
}

/* applying the animation */
div {
    animation: fadeInAnimation linear;
}
```

[View live example](http://03sq.net/examples/animation.html)

Example of an unprefixed @keyframes block that uses percentages to control the keyframes more exactly.

``` css
@keyframes bounceFadeInAnimation {
    /* starting state (same as "from") */
    0% {
        opacity: 0;
    }
    10% {
        opacity: 0.4;
    }
    15% {
        opacity: 0;
    }
    25% {
        opacity: 0.6;
    }
    50% {
        opacity: 0;
    }
    65% {
        opacity: 0.8;
    }
    80% {
        opacity: 0;
    }
    /* ending state (same as "to") */
    100% {
        opacity: 1;
    }
}
```

[View live example](http://03sq.net/examples/animation2.html)

## Notes

### Remarks

The version of this rule using a vendor prefix, **@-ms-keyframes**, has been deprecated. To ensure compatibility in the future, applications using this rule with a vendor prefix should be updated accordingly. This rule has no default value. This rule is used to specify property values at various points during an animation. The **@keyframes** rule specifies the property values during one cycle of an animation; the animation may iterate one or more times. This rule uses keyframe selectors to specify property values at various stages of the animation. Keyframe selectors can be declared as `from` (equivalent to `0%`), `to` (equivalent to `100%`), and one or more percentages. Keyframe selectors use keyframe descriptors to specify the properties and values being animated. If a property cannot be animated, the specification is ignored.

### Syntax

`@keyframes  <identifier>  {  <keyframes_blocks>  };`

### Parameters

*identifier*
:   The name of the animation.
*keyframes\_blocks*
:   A set of keyframes blocks, each of which is composed of keyframe selectors.

## Related specifications

[CSS Animations](http://www.w3.org/TR/css3-animations/#keyframes)
:   W3C Working Draft

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

-   **@keyframes**

-   [CSSKeyframeRule](/css/cssom/CSSKeyframeRule)

-   [keyText](/css/cssom/CSSKeyframeRule/keyText)

-   [style](/css/cssom/CSSKeyframeRule/style)

-   [CSSKeyframesRule](/css/cssom/CSSKeyframesRule)

-   [cssRules](/css/cssom/CSSKeyframesRule/cssRules)

-   [deleteRule](/css/cssom/CSSKeyframesRule/deleteRule)

-   [findRule](/css/cssom/CSSKeyframesRule/findRule)

-   [insertRule](/css/cssom/CSSKeyframesRule/insertRule)

-   [name](/css/cssom/CSSKeyframesRule/name)

-   [cubic-bezier](/css/functions/cubic-bezier)

-   [Animations](/css/properties/animations)

-   [transition](/css/properties/transition)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

#### Syntax

-   [@charset](/css/atrules/@charset)

-   [@font-face](/css/atrules/@font-face)

-   [@import](/css/atrules/@import)

-   **@keyframes**

-   [@namespace](/css/atrules/@namespace)

-   [@page](/css/atrules/@page)

-   [@supports](/css/atrules/@supports)

-   [CSS reference](/css/reference)

-   [Alphabetical list of CSS reference](/css/reference/alphabetical)

-   [!important](/css/syntax/!important)

### Other articles

-   [canIUse Compatibility Table](http://caniuse.com/#feat=css-animation)
-   [MDN](https://developer.mozilla.org/en-US/docs/CSS/@keyframes)

### Related pages (MSDN)

-   `animationName`
-   `css/properties/animation/animation`
