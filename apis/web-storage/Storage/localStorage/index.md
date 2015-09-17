---
title: 'localStorage'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
code_samples:
  - 'http://jsfiddle.net/DM6hB/6/'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/web-storage/Storage
    href: /apis/web-storage/Storage
  return:
    predicate: 'Returns an object of type '
    value: Object
    href: /apis/web-storage/Storage
standardization_status: 'W3C Proposed Recommendation'
summary: 'Provides a Storage object for an origin, that remains persistent even after restarting the browser. The storage can be cleared by the user with browser functionalities. If you need a temporary storage, use apis/web-storage/Storage/sessionStorage'
tags:
  - API_Object_Properties
  - Webstorage
uri: apis/web-storage/Storage/localStorage

---
## Summary

Provides a Storage object for an origin, that remains persistent even after restarting the browser. The storage can be cleared by the user with browser functionalities. If you need a temporary storage, use apis/web-storage/Storage/sessionStorage

Property of [apis/web-storage/Storage](/apis/web-storage/Storage)[apis/web-storage/Storage](/apis/web-storage/Storage)

## Syntax

**Note**: This property is read-only.

``` js
var result = object.localStorage;
```

## Return Value

Returns an object of type ObjectObject

## Examples

``` js
if (window.localStorage) { // checks if browser support localStorage
  if (localStorage['testKey']) { // checks if value exists
    console.log('Value exist on page load in localstorage for key testKey : ', localStorage['testKey']);
  }
  localStorage['testKey'] = 'Hi again!'; // stores value in localstorage
}
else {
 console.log('your browser dont support localstorage');
}
```

Fields and buttons for saving, reading and clearing localStorage items.

``` html
<section>
    <label for="key">Key:</label>
    <input type="text" id="key" value="r2d2">
    <br>
    <label for="value">Value:</label>
    <input type="text" id="value" value="C-3PO">
    <br>
    <button type="button" id="set-local">Save to localStorage</button>
</section>
<hr>
<section>
    <label for="get-key">Key:</label>
    <input type="text" id="get-key" value="r2d2">
    <button type="button" id="get-local">Get from localStorage</button>
    <output id="output"></output>
</section>
<hr>
<section>
    <button type="button" id="clear">Clear localStorage</button>
</section>
```

[View live example](http://jsfiddle.net/DM6hB/6/)

Functions and event handlers for saving, reading and clearing localStorage items.

``` js
/* global document, window */
var valueSetHandler = function () {
    /** read the values from the form */
    var key = document.getElementById('key').value,
        value = document.getElementById('value').value;

    /** save value under key in localStorage */
    window.localStorage.setItem(key, value);
},
valueGetHandler = function () {
    /** read the value from the form */
    var key = document.getElementById('get-key').value,

        /** read the value from the localStorage */
        value = window.localStorage.getItem(key);

    /** write the value in output */
    document.getElementById('output').innerText = value;
},
clearStorageHandler = function () {
    window.localStorage.clear();
};

/** register event Listeners for button clicks */
document.getElementById('set-local').addEventListener('click', valueSetHandler);
document.getElementById('get-local').addEventListener('click', valueGetHandler);
document.getElementById('clear').addEventListener('click', clearStorageHandler);
```

## Usage

     Use via the methods setItem, getItem, removeItem and clear provided by apis/web-storage/Storage.

Listen to the storage event on [dom/Window](/dom/Window) to catch changes in the storage (example: <http://jsfiddle.net/A6tuM/1/>).

## Notes

The **localStorage** "property" provides an instance of a storage area object, to which the **Storage** object's properties and methods are applied.

The amount of storage is limited by the browser on a per location basis (e.g. per domain). An error message is thrown, when the quota is exceed.

See for an example of the error message here (the example shows the error message for when the [sessionStorage](/apis/web-storage/Storage/sessionStorage) quota is exceeded. The behavior is similar for localStorage): <http://jsfiddle.net/wkDc6/1/>

## Related specifications

[W3C Web Storage Specification](http://www.w3.org/TR/webstorage/)
:   W3C Recommendation

## See also

### Related articles

#### Off-line Storage

-   [appcache](/apis/appcache)

-   [status](/apis/appcache/ApplicationCache/status)

-   [file](/apis/file)

-   [File System API](/apis/filesystem)

-   [quota management](/apis/quota_management)

-   [queryUsageAndQuota](/apis/quota_management/queryUsageAndQuota)

-   [requestQuota](/apis/quota_management/requestQuota)

-   **localStorage**

-   [Introduction to using the application cache](/tutorials/appcache_beginner)
