---
title: readAsText
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
notes:
  - 'Non-standard; deletion candidate'
readiness: 'Not Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/file/MSStreamReader
    href: /apis/file/MSStreamReader
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/file/MSStreamReader
standardization_status: Non-Standard
summary: 'Returns partial Blob data representing the number of bytes currently loaded (as a fraction of the total), decoded into memory according to the encoding determination.'
tags:
  0: API
  1: Object
  2: Methods
  4: FileAPI
uri: apis/file/MSStreamReader/readAsText

---
## <span>Summary</span>

Returns partial Blob data representing the number of bytes currently loaded (as a fraction of the total), decoded into memory according to the encoding determination.

Method of [apis/file/MSStreamReader](/apis/file/MSStreamReader)[apis/file/MSStreamReader](/apis/file/MSStreamReader)

## <span>Syntax</span>

``` js
var  = MSStreamReader.readAsText(/* see parameter list */);
```

## <span>Parameters</span>

### <span>stream</span>

 Data-type
:   any

### <span>encoding</span>

 Data-type
:   any

### <span>size</span>

 Data-type
:   any

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

This method can return one of these values.

S\_OK

**Needs Examples**: This section should include examples.

