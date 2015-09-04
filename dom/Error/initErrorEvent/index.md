---
title: initErrorEvent
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Not Ready'
notes:
  - 'Needs summary, examples, compat and spec link'
uri: dom/Error/initErrorEvent

---
# initErrorEvent

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [dom/Error](/dom/Error)*

## Syntax

``` {.js}
var object = object.initErrorEvent(typeArg, canBubbleArg, cancelableArg, messageArg, filenameArg, linenoArg);
```

## Parameters

### typeArg

 Data-typeÂ
:   any

 The type of the event being created

### canBubbleArg

 Data-typeÂ
:   any

 Indicates whether the event can bubble. When true the event should propagate upward. When false the event does not propagate upward.

### cancelableArg

 Data-typeÂ
:   any

 Indicates whether the eventâ€™s default action can be prevented. When true, the default action can be canceled. When false, the default action cannot be canceled.

### messageArg

 Data-typeÂ
:   any

 The error message string.

### filenameArg

 Data-typeÂ
:   any

 The absolute URL of the script in which the error originally occurred.

### linenoArg

 Data-typeÂ
:   unsigned long

 The line number where the error occurred in the script.

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

This method can return one of these values.

S\_OK

Type: **HRESULT**

This method can return one of these values.

S\_OK

**Needs Examples**: This section should include examples.

### Syntax

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

