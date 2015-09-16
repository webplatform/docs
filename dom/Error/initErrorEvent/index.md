---
title: 'initErrorEvent'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, examples, compat and spec link'
readiness: 'Not Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Error
    href: /dom/Error
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Error
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Error/initErrorEvent

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [dom/Error](/dom/Error)[dom/Error](/dom/Error)

## Syntax

``` js
var object = object.initErrorEvent(typeArg, canBubbleArg, cancelableArg, messageArg, filenameArg, linenoArg);
```

## Parameters

### typeArg

 Data-type
:   any

 The type of the event being created

### canBubbleArg

 Data-type
:   any

 Indicates whether the event can bubble. When true the event should propagate upward. When false the event does not propagate upward.

### cancelableArg

 Data-type
:   any

 Indicates whether the event’s default action can be prevented. When true, the default action can be canceled. When false, the default action cannot be canceled.

### messageArg

 Data-type
:   any

 The error message string.

### filenameArg

 Data-type
:   any

 The absolute URL of the script in which the error originally occurred.

### linenoArg

 Data-type
:   unsigned long

 The line number where the error occurred in the script.

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

This method can return one of these values.

S\_OK

Type: **HRESULT**

This method can return one of these values.

S\_OK

**Needs Examples**: This section should include examples.

### Syntax
