---
title: getAttribute
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/getAttribute8.htm'
notes:
  - 'Needs compat table'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Element
    href: /dom/Element
  return_type:
    predicate: 'Returns an object of type  '
    value: String
    href: /dom/Element
standardization_status: 'W3C Recommendation'
summary: 'Returns the value of the content attribute.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Element/getAttribute

---
## Summary

Returns the value of the content attribute.

Method of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## Syntax

``` js
var attributeValue = element.getAttribute(name);
```

## Parameters

### name

 Data-type
:   String

 The name of the attribute.

## Return Value

Returns an object of type StringString

The value of the attribute, or null if it does not exist.

## Examples

The following example shows the difference between a URL attribute which is using a content attribute (value from **getAttribute**) and a DOM attribute (property).

``` html
<!doctype html>
<head>
  <title>Content/DOM Attribute Example</title>
  <script>
    function GetAttr(){
     //Retrieve an element value from the content attribute and DOM attribute.
     var o = document.getElementById("msdn");

     var sContentAttr = o.getAttribute("href");
     var sDomAttr = o.href;

     var sOutput = ("Content attribute value: " + sContentAttr +
              "<br/>DOM attribute value: " + sDomAttr);
     document.getElementById("output").innerHTML = sOutput;
    }
  </script>
</head>
<body onload="GetAttr()">
   <a id="msdn" href="en-us/default.aspx">Microsoft Developer Network</a>
   <div id="output">Output appears here.</div>
</body>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/getAttribute8.htm)

## Usage

     Use this method to get the value of a content attribute of an element.

## Related specifications

[Document Object Model (DOM) Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

[Document Object Model (DOM) Level 2 Core](http://www.w3.org/TR/DOM-Level-2-Core/)
:   Recommendation

[Document Object Model (DOM) Level 1](http://www.w3.org/TR/REC-DOM-Level-1)
:   Recommendation

[DOM](http://dom.spec.whatwg.org/)
:   Living Standard

## See also

### Related pages

-   `removeAttribute`
-   `setAttribute`
