---
title: 'AnimationGroup'
readiness: 'In Progress'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: AnimationNode
    href: /apis/web_animations/AnimationNode
standardization_status: 'W3C Editor''s Draft'
summary: 'Animation groups are represented by the AnimationGroup interface.'
tags:
  - API
  - Objects
  - Web
  - Animations
uri: 'apis/web animations/AnimationGroup'

---
## Summary

Animation groups are represented by the AnimationGroup interface.

Inherits from [AnimationNode](/apis/web_animations/AnimationNode)[AnimationNode](/apis/web_animations/AnimationNode)

## Properties

API Name
:   Summary

[children](/apis/web_animations/AnimationGroup/children)
:   The list of child animation nodes in the group.

[firstChild](/apis/web_animations/AnimationGroup/firstChild)
:   The first child of this animation group.

[lastChild](/apis/web_animations/AnimationGroup/lastChild)
:   The last child of this animation group

## Methods

API Name
:   Summary

[append](/apis/web_animations/AnimationGroup/append)
:   If any of the animation nodes in nodes is an inclusive ancestor of this animation node throw a HierarchyRequestError exception and terminate these steps.

    Insert nodes before null.

[clone](/apis/web_animations/AnimationGroup/clone)
:   Creates a deep copy of this AnimationGroup object using the following procedure.

    Let source be this AnimationGroup object, the object to be cloned. Let cloned timing be a new AnimationTimingProperties object whose members are assigned the value of the attribute with the same name on source.timing. Let cloned children be an empty sequence of AnimationNode objects. For each child in source.children, append the result of calling child.clone() to cloned children. Return a new AnimationGroup object created by calling the AnimationGroup constructor with parameters AnimationGroup(cloned children, cloned timing).

[constructor](/apis/web_animations/AnimationGroup/constructor)
:

[prepend](/apis/web_animations/AnimationGroup/prepend)
:   If any of the animation nodes in nodes is an inclusive ancestor of this animation node throw a HierarchyRequestError exception and terminate these steps.

    Insert nodes before the first child.

## Events

*No events.*

## Inherited from AnimationNode

### Properties

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

### Methods

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

### Events

*No events.*

**Needs Examples**: This section should include examples.

