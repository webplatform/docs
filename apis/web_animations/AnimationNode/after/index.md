---
title: after
tags:
  - API
  - Object
  - Methods
  - Web
  - Animations
readiness: 'Almost Ready'
standardization_status: 'W3C Editor''s Draft'
summary: "Inserts nodes after this animation node.\n"
uri: 'apis/web animations/AnimationNode/after'

---
# after

## Summary

Inserts nodes after this animation node.

If there is no parent animation group, terminate these steps. If any of the animation nodes in nodes is an inclusive ancestor of this animation node throw a HierarchyRequestError exception and terminate these steps. Let reference child be the next sibling of this animation node not in nodes. Insert nodes before reference child.

*Method of [apis/web\_animations/AnimationNode](/apis/web_animations/AnimationNode)*

## Syntax

``` {.js}
var  = .after(AnimationNode...nodes);
```

## Parameters

### AnimationNode...nodes

 Data-typeÂ
:   Object

 Takes a series of AnimationNodes as a parameter

## Return Value

Returns an object of type .

**Needs Examples**: This section should include examples.

