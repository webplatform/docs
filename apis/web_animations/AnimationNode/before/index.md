---
title: 'before'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/web_animations/AnimationNode
    href: /apis/web_animations/AnimationNode
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/web_animations/AnimationNode
standardization_status: 'W3C Editor''s Draft'
summary: "Inserts nodes before this animation node.\n"
tags:
  - API
  - Object
  - Methods
  - Web
  - Animations
uri: 'apis/web animations/AnimationNode/before'

---
## Summary

Inserts nodes before this animation node.

If there is no parent animation group, terminate these steps. If any of the animation nodes in nodes is an inclusive ancestor of this animation node throw a HierarchyRequestError exception and terminate these steps. Insert nodes before this animation node. Note that this definition precludes the following usage since node is an inclusive ancestor of itself:

           node.before(node); // throws HierarchyRequestError


Method of [apis/web\_animations/AnimationNode](/apis/web_animations/AnimationNode)[apis/web\_animations/AnimationNode](/apis/web_animations/AnimationNode)

## Syntax

``` js
var  = .before(AnimationNode...nodes);
```

## Parameters

### AnimationNode...nodes

 Data-type
:   Object

 Takes a series of AnimationNodes as an object.

## Return Value

Returns an object of type

**Needs Examples**: This section should include examples.

