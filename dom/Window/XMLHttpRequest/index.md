---
title: 'XMLHttpRequest'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[XMLHttpRequest](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest) Article]'
  - 'Microsoft Developer Network: [[XMLHttpRequest Object](http://msdn.microsoft.com/en-us/library/ie/ms535874(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Window
    href: /dom/Window
  return:
    predicate: 'Returns an object of type '
    value: 'DOM Node'
    href: /dom/Window
standardization_status: 'W3C Working Draft'
summary: 'Represents an XML request using HTTP.'
tags:
  - API_Object_Properties
  - DOM
uri: dom/Window/XMLHttpRequest

---
## Summary

Represents an XML request using HTTP.

Property of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## Syntax

**Note**: This property is read-only.

``` js
var xhr = window.XMLHttpRequest;
```

## Return Value

Returns an object of type DOM NodeDOM Node

An XMLHttpRequest instance object.

## Examples

The following script demonstrates how to create and use the **XMLHttpRequest** object:

``` js
if (window.XMLHttpRequest)
{
  var xhr = new XMLHttpRequest();
  xhr.open("GET", "http://localhost/test.xml", true);
  xhr.onreadystatechange =
    function () {
      if (xhr.readyState === 4) {
        console.log(xhr.statusText);
     }
    };
   xhr.send();
}
```

## Usage

     It provides an easy way to retrieve data from a URL without having to do a full page refresh. A Web page can update just a part of the page without disrupting what the user is doing.  XMLHttpRequest is used heavily in AJAX programming.

## Related specifications

[XMLHttpRequest](http://www.w3.org/TR/XMLHttpRequest/)
:   Working Draft
