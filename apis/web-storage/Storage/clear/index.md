---
title: clear
tags:
  - API
  - Object
  - Methods
  - Webstorage
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Causes the list associated with the object to be emptied of all key/value pairs, if there are any.'
uri: apis/web-storage/Storage/clear

---
# clear

## Summary

Causes the list associated with the object to be emptied of all key/value pairs, if there are any.

*Method of [apis/web-storage/Storage](/apis/web-storage/Storage)*

## Syntax

``` {.js}
 object.clear();
```

## Return Value

No return value

## Examples

The following button clears the local storage area for the current domain.

``` {.html}
<button onclick="localStorage.clear()">
    Clear Stored Values</button>
```

## Notes

sessionStorage is cleared immediately. localStorage key/value pairs are removed from memory, and disk storage quota is updated.

## Related specifications

Specification
:   Status
[W3C Web Storage Specification](http://dev.w3.org/html5/webstorage)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

