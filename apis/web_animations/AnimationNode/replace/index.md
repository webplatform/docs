---
title: 'replace'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: 'apis/web animations/AnimationNode'
    href: /apis/web_animations/AnimationNode
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/web_animations/AnimationNode
standardization_status: 'W3C Editor''s Draft'
summary: "Replaces this AnimationNode with the passed in nodes.\n"
tags:
  - API_Object_Methods
  - Web_Animations
  - Needs_Examples
uri: 'apis/web animations/AnimationNode/replace'

---
## Summary

Replaces this AnimationNode with the passed in nodes.

If there is no parent animation group, terminate these steps. If any of the animation nodes in nodes is an inclusive ancestor of the parent animation group throw a HierarchyRequestError exception and terminate these steps. Let reference child be the next sibling of this animation node not in nodes. Remove this animation node from its parent animation group. Insert nodes before reference child.

Method of [apis/web animations/AnimationNode](/apis/web_animations/AnimationNode)[apis/web animations/AnimationNode](/apis/web_animations/AnimationNode)

## Syntax

``` js
var  = .replace();
```

## Return Value

Returns an object of type
