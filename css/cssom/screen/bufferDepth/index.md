---
title: bufferDepth
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, example, spec reference, standardization status'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/cssom/screen
    href: /css/cssom/screen
tags:
  - API
  - Object
  - Properties
  - DOM
uri: css/cssom/screen/bufferDepth

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [css/cssom/screen](/css/cssom/screen)[css/cssom/screen](/css/cssom/screen)

## <span>Syntax</span>

``` js
var result = element.bufferDepth;
element.bufferDepth = value;
```

**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

Nonsupported values cause **bufferDepth** to be set to **-1**. When **bufferDepth** is **-1** and the user changes system settings that affect the screen depth, the buffer depth is automatically updated to the new depth. This is not the case if **bufferDepth** is set to a specific value.

### <span>Syntax</span>

### <span>Standards information</span>

There are no standards that apply here.

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `screen`
