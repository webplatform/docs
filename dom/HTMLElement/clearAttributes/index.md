---
title: 'clearAttributes'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clearAttributes.htm'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/HTMLElement
tags:
  - API_Object_Methods
  - DOM
  - Needs_Summary
uri: dom/HTMLElement/clearAttributes

---
Method of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var object = object.clearAttributes();
```

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

This example uses the **clearAttributes** method to remove user-defined attributes from an element.

``` html
<SCRIPT>
function fnClear(){
   oSource.children[0].clearAttributes();
}
</SCRIPT>
<SPAN ID=oSource>
<DIV
   ID="oDiv"
   ATTRIBUTE1="true"
   ATTRIBUTE2="true"
   onclick="alert('click');"
   onmouseover="this.style.color='#0000FF';"
   onmouseout="this.style.color='#000000';"
>
This is a sample <b>DIV</b> element.
</DIV>
</SPAN>
<INPUT
   TYPE="button"
   VALUE="Clear Attributes"
   onclick="fnClear()"
>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clearAttributes.htm)

## Notes

### Remarks

The **clearAttributes** method clears only persistent HTML attributes. The ID attribute, styles, and script-only properties are not affected.

### Syntax

### Standards information

There are no standards that apply here.
