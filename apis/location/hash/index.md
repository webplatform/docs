---
title: 'window.location.hash'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/location
    href: /apis/location
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /apis/location
standardization_status: 'W3C Working Draft'
summary: 'The hash property contains the fragment identifier (including hash character) for the current page.'
tags:
  - API
  - Object
  - Properties
  - JavaScript
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/history
uri: apis/location/hash

---
## Summary

The hash property contains the fragment identifier (including hash character) for the current page.

Property of [apis/location](/apis/location)[apis/location](/apis/location)

## Syntax

``` js
var result = window.location.hash;
window.location.hash =
#foo;
```

## Return Value

Returns an object of type StringString

Returns the fragment identifier (including hash character) for the current page.

For example, `http://example.org/#foo` would return the fragment identifier of `#foo`.

## Examples

This example shows how to first check for the availability of the window.location.hash property, and then checks to see whether the second tab in our fictional web app should be displayed.

``` js
if(typeof window.location.hash != "undefined" && window.location.hash == "#tab2"){
    // Code to display the second tab goes here.
}
```

## Usage

     This property is used to see what the fragment identifier, or "hash" is for the current page is set to.

## Notes

The window.location.hash property does not work in versions of Internet Explorer prior to version 8.

This is most often used to preserve permalinks in web applications, however the [history API](/w/index.php?title=apis/history&action=edit&redlink=1) may be better suited to this task if legacy browser support is not required.

## Related specifications

[Window Object 1.0](http://www.w3.org/TR/Window/)
:   W3C Working Draft
