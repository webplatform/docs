---
title: Animation
readiness: 'Ready to Use'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: AnimationNode
    href: /apis/web_animations/AnimationNode
standardization_status: 'W3C Working Draft'
summary: 'Animations are represented by the Animation interface.'
tags:
  0: API
  1: Objects
  3: Web
  4: Animations
uri: 'apis/web animations/Animation'

---
## <span>Summary</span>

Animations are represented by the Animation interface.

Inherits from [AnimationNode](/apis/web_animations/AnimationNode)[AnimationNode](/apis/web_animations/AnimationNode)

## <span>Properties</span>

API Name
:   Summary

[effect](/apis/web_animations/Animation/effect)
:

[target](/apis/web_animations/Animation/target)
:

## <span>Methods</span>

API Name
:   Summary

[clone](/apis/web_animations/Animation/clone)
:   Creates a copy of an Animation object.

[constructor](/apis/web_animations/Animation/constructor)
:

## <span>Events</span>

*No events.*

## <span>Inherited from AnimationNode</span>

### <span>Properties</span>

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

### <span>Methods</span>

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

### <span>Events</span>

*No events.*

## <span>Related specifications</span>

[Web Animations 1.0](http://www.w3.org/TR/web-animations/)
:   W3C Working Draft
