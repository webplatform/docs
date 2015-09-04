---
title: clone
tags:
  - API
  - Object
  - Methods
  - Web
  - Animations
readiness: 'Almost Ready'
standardization_status: 'W3C Editor''s Draft'
summary: "Creates a deep copy of this AnimationGroup object using the following procedure.\n"
uri: 'apis/web animations/AnimationGroup/clone'

---
# clone

## Summary

Creates a deep copy of this AnimationGroup object using the following procedure.

Let source be this AnimationGroup object, the object to be cloned. Let cloned timing be a new AnimationTimingProperties object whose members are assigned the value of the attribute with the same name on source.timing. Let cloned children be an empty sequence of AnimationNode objects. For each child in source.children, append the result of calling child.clone() to cloned children. Return a new AnimationGroup object created by calling the AnimationGroup constructor with parameters AnimationGroup(cloned children, cloned timing).

*Method of [apis/web\_animations/AnimationGroup](/apis/web_animations/AnimationGroup)*

## Syntax

``` {.js}
var  = .clone();
```

## Return Value

Returns an object of type Object.

**Needs Examples**: This section should include examples.

