---
title: 'click'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/click.htm'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/HTMLElement
summary: 'Covers what the click action is and what happens when it is performed.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/HTMLElement/click

---
## Summary

Covers what the click action is and what happens when it is performed.

Method of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var object = object.click();
```

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

The following example demonstrates how simulating a click using the **click** does not, by default, bring the element into focus.

``` html
<!DOCTYPE html>
<html>
<head>
<title>onfocus Sample</title>
<link rel="stylesheet" type="text/css" href="samplesSDKIE4.css" />
</head>
<body>
  <p>DEMO: USING CLICK METHOD DOES NOT SET FOCUS<p>
    <ul>
      <li>Both these buttons apply the click method to the check box. </li>
      <li>An alert has been set to fire when the check box is put into focus.</li>
    </ul>
  </p>
  <input type="checkbox" id="chk1"/>
    <br>
    <button onclick="simclick1()">This button <strong>applies the focus method</strong> to
      check box</button>
    <br>
    <button onclick="simclick2()">This button <strong>does not apply the focus method</strong> to check box</button>
    <br>

  <script>
    // When chk1 gets focus, pop an alert
    document.getElementById("chk1").addEventListener("focus", function(){alert("check box is in focus!");}, false);
    function simclick1() {
      chk1.focus(); //focus is explicitly set
      chk1.click();
    }
    function simclick2() {
      chk1.click();
    }
  </script>
</body>
</html>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/click.htm)

## Notes

### Remarks

**Note**  Simulating a click using the **click** does not bring the element being clicked into focus. (See example below).

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.6.5
