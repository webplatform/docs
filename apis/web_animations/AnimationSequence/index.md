---
title: 'AnimationSequence'
readiness: 'In Progress'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: AnimationGroup
    href: /apis/web_animations/AnimationGroup
standardization_status: 'W3C Editor''s Draft'
summary: 'Animation sequences are represented by the AnimationSequence interface.'
tags:
  - API
  - Objects
  - Web
  - Animations
uri: 'apis/web animations/AnimationSequence'

---
## Summary

Animation sequences are represented by the AnimationSequence interface.

Inherits from [AnimationGroup](/apis/web_animations/AnimationGroup)[AnimationGroup](/apis/web_animations/AnimationGroup)

## Properties

*No properties.*

## Methods

*No methods.*

## Events

*No events.*

## Inherited from AnimationGroup

### Properties

API Name
:   Summary

[children](/apis/web_animations/AnimationGroup/children)
:   The list of child animation nodes in the group.

[firstChild](/apis/web_animations/AnimationGroup/firstChild)
:   The first child of this animation group.

[lastChild](/apis/web_animations/AnimationGroup/lastChild)
:   The last child of this animation group

### Methods

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

### Events

*No events.*

**Needs Examples**: This section should include examples.

