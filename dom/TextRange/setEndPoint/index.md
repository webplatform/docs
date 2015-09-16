---
title: 'setEndPoint'
attributions:
  - 'Microsoft Developer Network: [[setEndPoint Method](http://msdn.microsoft.com/en-us/library/ie/ms536745(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/TextRange
    href: /dom/TextRange
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /dom/TextRange
standardization_status: Non-Standard
summary: 'Sets the endpoint of one range based on the endpoint of another range.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/TextRange/setEndPoint

---
## Summary

Sets the endpoint of one range based on the endpoint of another range.

Method of [dom/TextRange](/dom/TextRange)[dom/TextRange](/dom/TextRange)

## Syntax

``` js
var result = textRange.setEndPoint(/* see parameter list */);
```

## Parameters

### how

 Data-type
:   BSTR

**String** that specifies the endpoint to transfer using one of the following values.

StartToEnd

Move the start of the TextRange object to the end of the specified SourceRange parameter.

StartToStart

Move the start of the TextRange object to the start of the specified SourceRange parameter.

EndToStart

Move the end of the TextRange object to the start of the specified SourceRange parameter.

EndToEnd

Move the end of the TextRange object to the end of the specified SourceRange parameter.

### SourceRange

 Data-type
:   any

[**TextRange**](/dom/TextRange) object from which the source endpoint is to be taken.

## Return Value

Returns an object of type

## Examples

The following example shows how to use the **setEndPoint** method to set the start point of the current range (`r1`) to the endpoint of the second range (`r2`).

``` js
<script type="text/javascript">
r1.setEndPoint("StartToEnd", r2);
</script>
```

## Notes

### Syntax

var retval = TextRange.setEndPoint(how, SourceRange);

### Remarks

A text range has two endpoints: one at the beginning of the text range and one at the end. An endpoint can also be the position between two characters in an HTML document. There are four possible endpoint locations in the following HTML.

    <BODY><P><B>abc

The possible endpoint locations are:

-   Before the letter a.
-   Between the letters a and b.
-   Between the letters b and c.
-   After the letter c.

This feature might not be available on platforms other than Microsoft Win32. In Microsoft Internet Explorer 4.0, an endpoint is relative to text only, not HTML tags. In Internet Explorer 4.0, an endpoint cannot be established between **body** and **p**. Specifying an endpoint between **body** and **p** is interpreted as if it occurs before the letter a.
