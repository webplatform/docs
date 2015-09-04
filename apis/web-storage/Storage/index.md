---
title: Storage
tags:
  - API
  - Objects
  - Webstorage
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Provides access to a list of key/value pairs, sometimes called "items". The amount of storage space is limited by browsers. Changes fire ''storage'' event on dom/Window.'
code_samples:
  - 'http://playground.html5rocks.com/#localstorage'
  - 'http://jsfiddle.net/A6tuM/1/'
uri: apis/web-storage/Storage

---
# Storage

## Summary

Provides access to a list of key/value pairs, sometimes called "items". The amount of storage space is limited by browsers. Changes fire 'storage' event on dom/Window.

## Properties

API Name
:   Summary
[length](/apis/web-storage/Storage/length)
:   Returns the number of key/value pairs currently present in the list associated with the object.
[localStorage](/apis/web-storage/Storage/localStorage)
:   Provides a Storage object for an origin, that remains persistent even after restarting the browser. The storage can be cleared by the user with browser functionalities. If you need a temporary storage, use [apis/web-storage/Storage/sessionStorage](/apis/web-storage/Storage/sessionStorage)
[sessionStorage](/apis/web-storage/Storage/sessionStorage)
:   Provides a Storage object specific to the current top-level browsing context. The storage will be cleared after a browser restart. If you need a persistent storage, use [apis/web-storage/Storage/localStorage](/apis/web-storage/Storage/localStorage).

## Methods

API Name
:   Summary
[clear](/apis/web-storage/Storage/clear)
:   Causes the list associated with the object to be emptied of all key/value pairs, if there are any.
[getItem](/apis/web-storage/Storage/getItem)
:   Returns the current value associated with the given key.
[key](/apis/web-storage/Storage/key)
:   Returns the name of the *n*th key in the list.
[removeItem](/apis/web-storage/Storage/removeItem)
:   Removes the key/value pair with the given key from the list associated with the object, if it exists.
[setItem](/apis/web-storage/Storage/setItem)
:   Adds or replaces a value for the given key.

## Events

*No events.*

## Examples

Key names are exposed as properties on this object. For example, the following statements are equivalent:

``` {.js}
sessionStorage.setItem('myKey', '...');

sessionStorage['myKey'] = '...';

sessionStorage.myKey = '...';
```

``` {.html}
<html>
  <head>
    <style>
    </style>
  </head>

  <body>

    <div id="example-excerpt">
      This sample saves some text on the localStorage object
      and retrieves the value on load time.
      Use your browser developer tools to debug the
      values of the localStorage object.
    </div>

    <div id="example-content"></div>

    <p id="log"></p>

    <!-- Javscript -->

  </body>
</html>
```

[View live example](http://playground.html5rocks.com/#localstorage)

``` {.css}
body {
      font: 100% "Lucida Grande", "Trebuchet MS", Verdana, sans-serif;
      margin: 0;
    }

    #log {
      background-color: gray;
      color: white;
      padding: 10px;
      margin-left: 20px;
      display: inline-block;
    }

    header {
      background: #FFCC99;
      color: white;
      -moz-box-shadow: 0 2px 8px -3px rgba(0,0,0,.5), 0 1.4em 2em -0.7em rgba(255, 255, 255, .2) inset;
      -webkit-box-shadow: 0 2px 8px -3px rgba(0,0,0,.5), 0 1.4em 2em -0.7em rgba(255, 255, 255, .2) inset;
      box-shadow: 0 2px 8px -3px rgba(0,0,0,.5), 0 1.4em 2em -0.7em rgba(255, 255, 255, .2) inset;
      text-shadow: 1px 1px 1px #444;
    }

    header h1, header h2 {
      display: inline-block;
      padding: 12px 15px;
      font-size: 105%;
      line-height: 1;
      margin: 0;
    }

    header h1 {
      background: #FF9966;
    }

    #excerpt {
      padding: 20px;
      background: #fcfaea;
    }

    .arrow-right {
      display: inline-block;
      width: 0;
      height: 0;
      border-top: 18px solid transparent;
      border-bottom: 18px solid transparent;
      border-left: 18px solid #FF9966;
      margin-bottom: -11px;
    }

    #content {
      padding: 20px;
      color: #333;
    }

    input, textarea {
      font-size: 100%;
    }
```

``` {.js}
// Generate the little markup from javascript

document.querySelector('#content').innerHTML =
          '<p><em>Save text locally (it will still be available
          after restarting your browser)</em></p>';

var area = document.createElement('textarea');
    area.style.width = '300px';
    area.style.height = '150px';
      document.querySelector('#content').appendChild(area);

      // place content from previous edit
      if (!area.value) {
        area.value = window.localStorage.getItem('value');
      }

      // your content will be saved locally
      area.addEventListener('keyup', function () {
        window.localStorage.setItem('value', area.value);
        window.localStorage.setItem('timestamp', (new Date()).getTime());
      }, false);

      updateLog();
      setInterval(updateLog, 5000); // show time every 5 seconds

      function updateLog() {
        var delta = 0;
        if (window.localStorage.getItem('value')) {
          delta = ((new Date()).getTime() -
            (new Date()).setTime(window.localStorage.getItem
            ('timestamp'))) / 1000;
          document.querySelector("#log").innerHTML = 'last saved: ' + delta + 's ago';
        }
        else {
          area.value = 'Type your text here...';
        }
      }
```

An example on how to listen to changes in the localStorage. The example can be applied to sessionStorage as well. A full example is in the fiddle.

``` {.js}
// this event is only fired in browser windows, that did not initiated the change. Thus the fiddle uses two iframes to show how the event is fired.
window.addEventListener('storage', function (event) {
    // logs the key that has changed and the old and the new value in the storage
    console.log(event.key, event.oldValue, event.newValue);
});
```

[View live example](http://jsfiddle.net/A6tuM/1/)

## Notes

Each **Storage** object provides access to a list of key/value pairs, which are sometimes called items. Keys are strings, and any string (including the empty string) is a valid key. Items contain values (which are also strings) and associated metadata.

Each **Storage** object is associated with a list of key/value pairs when it is created. Multiple **Storage** objects, such as two instances of **localStorage**, can be associated with the same list of key/value pairs simultaneously.

The **amount of storage** is **limited** by the browser (quota). An error is thrown, when the quota is exceeded. An example, that intentionally exceeds the quota and throws and error may be found here: [http://jsfiddle.net/wkDc6/1/](http://jsfiddle.net/wkDc6/1/)

## Related specifications

Specification
:   Status
[W3C Web Storage Specification](http://www.w3.org/TR/webstorage/)
:   W3C Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

Portions of this content come from HTML5Rocks! [article](http://playground.html5rocks.com/#localstorage)

