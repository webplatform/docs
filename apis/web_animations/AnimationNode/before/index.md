---
title: before
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
## <span>Summary</span>

Inserts nodes before this animation node.

If there is no parent animation group, terminate these steps. If any of the animation nodes in nodes is an inclusive ancestor of this animation node throw a HierarchyRequestError exception and terminate these steps. Insert nodes before this animation node. Note that this definition precludes the following usage since node is an inclusive ancestor of itself:

           node.before(node); // throws HierarchyRequestError


Method of [apis/web\_animations/AnimationNode](/apis/web_animations/AnimationNode)[apis/web\_animations/AnimationNode](/apis/web_animations/AnimationNode)

## <span>Syntax</span>

``` js
var  = .before(AnimationNode...nodes);
```

## <span>Parameters</span>

### <span>AnimationNode...nodes</span>

 Data-type
:   Object

 Takes a series of AnimationNodes as an object.

## <span>Return Value</span>

Returns an object of type<span></span>

**Needs Examples**: This section should include examples.

