---
title: msWriteProfilerMark
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Not Ready'
standardization_status: Non-Standard
notes:
  - 'Not part of user_timing, resource_timing, or navigation_timing interfaces. Needs summary; non-standard; deletion candidate.'
uri: apis/timing/methods/msWriteProfilerMark
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/workers/objects/WorkerGlobalScope

---
# msWriteProfilerMark

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [dom/Element](/dom/Element)*

## Syntax

``` {.js}
var object = object.msWriteProfilerMark(/* see parameter list */);
```

## Parameters

### bstrProfilerMarkName

 Data-type�
:   any

 An event name. This parameter may be null.

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

**Needs Examples**: This section should include examples.

## Notes

### Remarks

Internet Explorer 10. This method is also available in the Web Worker global scope. For Windows XP, this method sends an event to an event tracing session with TraceEvent; for systems after Windows XP, this method writes an event with EventWrite. The event includes a pointer to a **window** object, current markup, and the event name passed as *bstrProfilerMarkName*. The *bstrProfilerMarkName* property has a 32-character limit when called from script. This method is useful to profile real website performance by using the operating system metrics as a baseline.

### Syntax

### Standards information

There are no standards that apply here.

## See also

### Related pages (MSDN)

-   `window`
-   `WorkerGlobalScope`
-   `Windows Events`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

