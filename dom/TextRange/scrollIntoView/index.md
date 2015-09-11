---
title: scrollIntoView
attributions:
  - 'Microsoft Developer Network: [[scrollIntoView Method](http://msdn.microsoft.com/en-us/library/ie/ms536730(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/TextRange
    href: /dom/TextRange
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/TextRange
standardization_status: Non-Standard
summary: 'Causes the object to scroll into view, aligning it either at the top or bottom of the window. '
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/TextRange/scrollIntoView

---
## <span>Summary</span>

Causes the object to scroll into view, aligning it either at the top or bottom of the window.

Method of [dom/TextRange](/dom/TextRange)[dom/TextRange](/dom/TextRange)

## <span>Syntax</span>

``` js
var result = node.scrollIntoView(/* see parameter list */);
```

## <span>Parameters</span>

### <span>varargStart</span>

 Data-type
:   VARIANT

**Variant** of type **Boolean** that specifies one of the following values:

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## <span>Examples</span>

This example uses the **scrollIntoView** method to underline the content of the document's fifth paragraph and scroll it into view at the top of the window.

``` js
var coll = document.all.tags("P");
   if (coll.length >= 5)
   {
      coll(4).style.textDecoration = "underline";
      coll(4).scrollIntoView(true);
   }
```

## <span>Usage</span>

     The scrollIntoView method is useful for immediately showing the user the result of some action without requiring the user to manually scroll through the document to find the result.

## <span>Notes</span>

### <span>Remarks</span>

Depending on the size of the given object and the current window, this method might not be able to put the item at the very top or very bottom, but will position the object as close to the requested position as possible.