---
title: 'bufferDepth'
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
  - API_Object_Properties
  - DOM
  - Needs_Summary
  - Needs_Examples
uri: css/cssom/screen/bufferDepth

---
Property of [css/cssom/screen](/css/cssom/screen)[css/cssom/screen](/css/cssom/screen)

## Syntax

``` js
var result = element.bufferDepth;
element.bufferDepth = value;
```

## Notes

### Remarks

Nonsupported values cause **bufferDepth** to be set to **-1**. When **bufferDepth** is **-1** and the user changes system settings that affect the screen depth, the buffer depth is automatically updated to the new depth. This is not the case if **bufferDepth** is set to a specific value.

### Syntax

### Standards information

There are no standards that apply here.

## See also

### Related pages

-   screen[screen](/css/cssom/screen)
