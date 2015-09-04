---
title: hash
tags:
  - API
  - Object
  - Properties
  - JavaScript
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The hash property contains the fragment identifier (including hash character) for the current page.'
uri: apis/location/hash
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/history

---
# window.location.hash

## Summary

The hash property contains the fragment identifier (including hash character) for the current page.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/location](/apis/location)</span></span>

## Syntax

``` {.js}
var result = window.location.hash;
window.location.hash =
#foo;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

Returns the fragment identifier (including hash character) for the current page.

For example, `http://example.org/#foo` would return the fragment identifier of `#foo`.

## Examples

This example shows how to first check for the availability of the window.location.hash property, and then checks to see whether the second tab in our fictional web app should be displayed.

``` {.js}
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

Specification
:   Status
[Window Object 1.0](http://www.w3.org/TR/Window/)
:   W3C Working Draft

