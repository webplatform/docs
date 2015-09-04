---
title: sessionStorage
tags:
  - API
  - Object
  - Properties
  - Webstorage
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Provides a Storage object specific to the current top-level browsing context. The storage will be cleared after a browser restart. If you need a persistent storage, use apis/web-storage/Storage/localStorage.'
code_samples:
  - 'http://jsfiddle.net/DM6hB/7/'
uri: apis/web-storage/Storage/sessionStorage

---
# sessionStorage

## Summary

Provides a Storage object specific to the current top-level browsing context. The storage will be cleared after a browser restart. If you need a persistent storage, use apis/web-storage/Storage/localStorage.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/web-storage/Storage](/apis/web-storage/Storage)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = object.sessionStorage;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Object</span></span>

## Examples

``` {.js}
/* global document, window */

var valueSetHandler = function () {
    /** read the values from the form */
    var key = document.getElementById('key').value,
        value = document.getElementById('value').value;

    /** save value under key in localStorage */
    window.sessionStorage.setItem(key, value);
},
valueGetHandler = function () {
    /** read the value from the form */
    var key = document.getElementById('get-key').value,

        /** read the value from the localStorage */
        value = window.sessionStorage.getItem(key);

    /** write the value in output */
    document.getElementById('output').innerText = value;
},
clearStorageHandler = function () {
    window.sessionStorage.clear();
};

/** register event Listeners for button clicks */
document.getElementById('set-local').addEventListener('click', valueSetHandler);
document.getElementById('get-local').addEventListener('click', valueGetHandler);
document.getElementById('clear').addEventListener('click', clearStorageHandler);
```

[View live example](http://jsfiddle.net/DM6hB/7/)

``` {.html}
<section>
    <label for="key">Key:</label>
    <input type="text" id="key" value="c3po">

    <label for="value">Value:</label>
    <input type="text" id="value" value="R2-D2">

    <button type="button" id="set-local">Save to sessionStorage</button>
</section>
<section>

   <label for="get-key">Key:</label>
   <input type="text" id="get-key" value="c3po">
   <button type="button" id="get-local">Get from sessionStorage</button>
   <output id="output"></output>
```

\</section\>

* * * * *

\<section\>

       <button type="button" id="clear">Clear sessionStorage</button>

\</section\>

</pre>

## Usage

     Use the methods setItem, getItem, removeItem and clear defined in apis/web-storage/Storage

## Notes

The **sessionStorage** "property" provides an instance of a storage area object, to which the **Storage** object's properties and methods are applied.

The amount of storage in sessionStorage is limited by a quota by the browser. See an example error for when the quota is exceed: [http://jsfiddle.net/wkDc6/1/](http://jsfiddle.net/wkDc6/1/)

## Related specifications

Specification
:   Status
[W3C Web Storage Specification](http://dev.w3.org/html5/webstorage)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

