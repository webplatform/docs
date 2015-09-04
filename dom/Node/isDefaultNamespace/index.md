---
title: isDefaultNamespace
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Indicates whether or not a namespace is the default namespace for a document.'
uri: dom/Node/isDefaultNamespace

---
# isDefaultNamespace

## Summary

Indicates whether or not a namespace is the default namespace for a document.

*Method of [dom/Node](/dom/Node)*

## Syntax

``` {.js}
var isDefault = node.isDefaultNamespace(/* see parameter list */);
```

## Parameters

### namespace

 Data-typeÂ
:   String

 The namespace to be compared to the default namespace.

## Return Value

Returns an object of type Boolean.

Whether the namespace specified in the *namespace* parameter is the default namespace for the document.

## Examples

The following example compares the default Namespace of the body element to the SVG namespace and then to the xHTML namespace. false then true is displayed.

    <!DOCTYPE html>
    <html>

    <head>
    <meta content="text/html; charset=utf-8" http-equiv="Content-Type">
    <title>isDefaultNamespace example</title>
    </head>

    <body>


       <script type="text/javascript">//<![CDATA[
        var nsSVG='http://www.w3.org/2000/svg';
        alert(document.body.isDefaultNamespace(nsSVG));
        var nsxHTML='http://www.w3.org/1999/xhtml';
        alert(document.body.isDefaultNamespace(nsxHTML));
       //]]></script>
    </body>

    </html>

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.isDefaultNamespace](https://developer.mozilla.org/en-US/docs/Web/API/Node.isDefaultNamespace) Article]

Portions of this content come from the Microsoft Developer Network: [[isDefaultNamespace Method](http://msdn.microsoft.com/en-us/library/ie/ff975127(v=vs.85).aspx) Article]

