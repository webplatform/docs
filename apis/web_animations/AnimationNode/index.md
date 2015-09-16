---
title: 'AnimationNode'
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
summary: 'Animation nodes are represented in the Web Animations API by the AnimationNode interface.'
tags:
  0: API
  1: Objects
  3: Web
  4: Animations
uri: 'apis/web animations/AnimationNode'

---
## Summary

Animation nodes are represented in the Web Animations API by the AnimationNode interface.

## Properties

API Name
:   Summary

[computedTiming](/apis/web_animations/AnimationNode/computedTiming)
:   Returns the calculated timing properties for this animation node. This is comparable to the computed style of an Element, window.getComputedStyle(elem).

    Although several of the attributes of the this object are common to the AnimationTiming object returned by the timing attribute, they have the following differences:

    duration – returns the calculated value of the iteration duration. If timing.duration is the string auto or any unsupported value, this attribute will return the current calculated value of the intrinsic iteration duration. fill – the auto value is replaced with the specific FillMode depending on the type of animation node (see §5.8.1 The FillMode enumeration). easing – unrecognised or unsupported values are replaced with the string linear.

[nextSibling](/apis/web_animations/AnimationNode/nextSibling)
:   The next sibling of this animation node.

[parent](/apis/web_animations/AnimationNode/parent)
:   The parent animation group of this animation node or null if this animation node does not have a parent animation group.

[previousSibling](/apis/web_animations/AnimationNode/previousSibling)
:   The previous sibling of this animation node.

[timing](/apis/web_animations/AnimationNode/timing)
:   Returns the input timing properties specified for this animation node. This is comparable to the specified style on an Element, elem.style.

## Methods

API Name
:   Summary

[after](/apis/web_animations/AnimationNode/after)
:   Inserts nodes after this animation node.

    If there is no parent animation group, terminate these steps. If any of the animation nodes in nodes is an inclusive ancestor of this animation node throw a HierarchyRequestError exception and terminate these steps. Let reference child be the next sibling of this animation node not in nodes. Insert nodes before reference child.

[before](/apis/web_animations/AnimationNode/before)
:   Inserts nodes before this animation node.

    If there is no parent animation group, terminate these steps. If any of the animation nodes in nodes is an inclusive ancestor of this animation node throw a HierarchyRequestError exception and terminate these steps. Insert nodes before this animation node. Note that this definition precludes the following usage since node is an inclusive ancestor of itself:

               node.before(node); // throws HierarchyRequestError

[remove](/apis/web_animations/AnimationNode/remove)
:   Removes this animation node from its parent animation group or player.

[replace](/apis/web_animations/AnimationNode/replace)
:   Replaces this AnimationNode with the passed in nodes.

    If there is no parent animation group, terminate these steps. If any of the animation nodes in nodes is an inclusive ancestor of the parent animation group throw a HierarchyRequestError exception and terminate these steps. Let reference child be the next sibling of this animation node not in nodes. Remove this animation node from its parent animation group. Insert nodes before reference child.

## Events

*No events.*

**Needs Examples**: This section should include examples.

## Related specifications

[ ]
:

## See also

### Related articles

#### Animation

-   [Web Animations API](/apis/web_animations)

-   [clone](/apis/web_animations/AnimationEffect/clone)

-   **AnimationNode**

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

-   [cubic-bezier](/css/functions/cubic-bezier)

-   [Animations](/css/properties/animations)

-   [transition](/css/properties/transition)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)
