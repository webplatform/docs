---
title: after
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
summary: "Inserts nodes after this animation node.\n"
tags:
  - API
  - Object
  - Methods
  - Web
  - Animations
uri: 'apis/web animations/AnimationNode/after'

---
## <span>Summary</span>

Inserts nodes after this animation node.

If there is no parent animation group, terminate these steps. If any of the animation nodes in nodes is an inclusive ancestor of this animation node throw a HierarchyRequestError exception and terminate these steps. Let reference child be the next sibling of this animation node not in nodes. Insert nodes before reference child.

Method of [apis/web\_animations/AnimationNode](/apis/web_animations/AnimationNode)[apis/web\_animations/AnimationNode](/apis/web_animations/AnimationNode)

## <span>Syntax</span>

``` js
var  = .after(AnimationNode...nodes);
```

## <span>Parameters</span>

### <span>AnimationNode...nodes</span>

 Data-type
:   Object

 Takes a series of AnimationNodes as a parameter

## <span>Return Value</span>

Returns an object of type<span></span>

**Needs Examples**: This section should include examples.

