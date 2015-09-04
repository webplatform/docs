---
title: normalize
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Merges adjacent DOM objects to produce a normalized document object model.'
uri: dom/Node/normalize

---
# normalize

## Summary

Merges adjacent DOM objects to produce a normalized document object model.

*Method of [dom/Node](/dom/Node)*

## Syntax

``` {.js}
 node.normalize();
```

## Return Value

No return value

## Examples

    <!DOCTYPE html>
    <html>
    <head>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>
    <title>Node.normalize() example</title>
    </head>

    <body>


    <script type="text/javascript">
    var wrapper = document.createElement("div");

    wrapper.appendChild( document.createTextNode("Part 1 ") );
    wrapper.appendChild( document.createTextNode("Part 2 ") );

    // At this point, wrapper.childNodes.length === 2
    // wrapper.childNodes[0].textContent === "Part 1 "
    // wrapper.childNodes[1].textContent === "Part 2 "
    alert('wrapper.childNodes.length==='+wrapper.childNodes.length);
    wrapper.normalize();
    document.body.appendChild(wrapper);
    // Now, wrapper.childNodes.length === 1
    // wrapper.childNodes[0].textContent === "Part 1 Part 2 "
    alert('wrapper.normalize();wrapper.childNodes.length==='+wrapper.childNodes.length);

    </script>

    </body>
    </html>

## Usage

     By calling object.normalize before the subelements of an object are manipulated, you ensure that the document object model has a consistent structure.  The normal form is useful for operations that require a consistent document tree structure, and it ensures that the document object model view is identical when it is saved and reloaded.

## Notes

The **normalize** method does not merge adjacent **CDATA** sections, allowing for an inconsistent object model when **CDATA** sections are present.

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.normalize](https://developer.mozilla.org/en-US/docs/Web/API/Node.normalize) Article]

Portions of this content come from the Microsoft Developer Network: [[normalize Method](http://msdn.microsoft.com/en-us/library/ie/ms536646(v=vs.85).aspx) Article]

