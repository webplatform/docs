---
title: clone
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/web_animations/AnimationGroup
    href: /apis/web_animations/AnimationGroup
  return_type:
    predicate: 'Returns an object of type  '
    value: Object
    href: /apis/web_animations/AnimationGroup
standardization_status: 'W3C Editor''s Draft'
summary: "Creates a deep copy of this AnimationGroup object using the following procedure.\n"
tags:
  - API
  - Object
  - Methods
  - Web
  - Animations
uri: 'apis/web animations/AnimationGroup/clone'

---
## <span>Summary</span>

Creates a deep copy of this AnimationGroup object using the following procedure.

Let source be this AnimationGroup object, the object to be cloned. Let cloned timing be a new AnimationTimingProperties object whose members are assigned the value of the attribute with the same name on source.timing. Let cloned children be an empty sequence of AnimationNode objects. For each child in source.children, append the result of calling child.clone() to cloned children. Return a new AnimationGroup object created by calling the AnimationGroup constructor with parameters AnimationGroup(cloned children, cloned timing).

Method of [apis/web\_animations/AnimationGroup](/apis/web_animations/AnimationGroup)[apis/web\_animations/AnimationGroup](/apis/web_animations/AnimationGroup)

## <span>Syntax</span>

``` js
var  = .clone();
```

## <span>Return Value</span>

Returns an object of type ObjectObject

**Needs Examples**: This section should include examples.

