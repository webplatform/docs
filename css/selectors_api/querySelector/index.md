---
title: 'querySelector'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Element
    href: /dom/Element
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Element
summary: 'Returns the first element that matches the provided selector.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: 'css/selectors api/querySelector'

---
## Summary

Returns the first element that matches the provided selector.

Method of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## Syntax

``` js
var element = element.querySelector(/* see parameter list */);
```

## Parameters

### selectors

 Data-type
:   String

 A selector, or multiple selectors (separated by commas).

## Return Value

Returns an object of type DOM NodeDOM Node

A DOM element node, or null if the search cannot find an element that matches the selector string.

## Examples

This example illustrates how the selectors in the selector string are scoped to the entire document. The variable `e` contains the span even though the provided selector references the P element, which is outside the scope of the starting DIV element.

``` html
<!doctype html>
<html>
<!-- To limit the search to descendants of an element only, -->
<!-- call the selectors API on the specific element of interest. -->
<body>
    <p>
        <div id="apple">
        Some are sauce, some are pie.
        </div>
    </p>
<script>
    var div = document.getElementById("apple");
    var   e = div.querySelector("p span");    // 'e' will select the span.
    var   f = div.querySelector("p div");     // 'f' will be null because the div is not a descendent of 'div'
</script>
</body>
</html>
```

## Notes

The document search order is depth-first. This method returns the first element found. To find all matching nodes, use [**querySelectorAll**](/css/selectors_api/querySelectorAll). The scope of the returned element node is limited to the descendants of the starting element node. If the starting element is [Document](/dom/Document), the search returns nodes from the entire document. This method does not return the starting element node. For example, `div.querySelector("p div")` will never return the **DIV** element that it starts with. The pseudo-class selectors [**:hover**](/css/selectors/pseudo-classes/:hover), [**:focus**](/css/selectors/pseudo-classes/:focus), and [**:active**](/css/selectors/pseudo-classes/:active) are supported. Selectors that contain [**:visited**](/css/selectors/pseudo-classes/:visited) or [**:link**](/css/selectors/pseudo-classes/:link) are ignored and no elements are returned. You can search namespaced elements using a selector syntax based on prefix instead of the namespaceURI, for example "nsPrefix \\: element", where "nsPrefix" is the prefix of a given element. Selectors are described in detail in Understanding CSS Selectors and [W3C Selectors](http://www.w3.org/TR/css3-selectors/). Calling this method with an unknown selector (due to the browser not implementing it, or due to typo and such) may throw an exception.

## Related specifications

[Selectors API Level 1](http://www.w3.org/TR/selectors-api)
:   Proposed Recommendation

## See also

### Related pages

-   [Document](/dom/Document)
-   [a](/html/elements/a)
-   `address`
-   `b`
-   `big`
-   `blockQuote`
-   `body`
-   `button`
-   `caption`
-   `center`
-   `cite`
-   `code`
-   `col`
-   `colGroup`
-   `dd`
-   `dfn`
-   `dir`
-   `div`
-   `dl`
-   `dt`
-   `em`
-   `fieldSet`
-   `form`
-   `hn`
-   `html`
-   `i`
-   `img`
-   `input type=button`
-   `input type=checkbox`
-   `input type=file`
-   `input type=image`
-   `input type=password`
-   `input type=radio`
-   `input type=reset`
-   `input type=submit`
-   `input type=text`
-   `isIndex`
-   `kbd`
-   `label`
-   `legend`
-   `li`
-   `listing`
-   `marquee`
-   `menu`
-   `noBR`
-   `ol`
-   `p`
-   `plainText`
-   `pre`
-   `s`
-   `samp`
-   `small`
-   `span`
-   `strike`
-   `strong`
-   `sub`
-   `sup`
-   [table](/html/elements/table)
-   `tBody`
-   `td`
-   `textArea`
-   `tFoot`
-   `th`
-   `tHead`
-   `tr`
-   `tt`
-   `u`
-   `ul`
-   `var`
-   `xmp`
-   `Reference`
-   [querySelectorAll](/css/selectors_api/querySelectorAll)
-   `Other Resources`
-   [[W3C Selectors API](http://go.microsoft.com/fwlink/p/?linkid=203783)]
-   [[W3C Selectors](http://go.microsoft.com/fwlink/p/?linkid=203764)]
