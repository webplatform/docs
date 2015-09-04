---
title: async
tags:
  - Markup
  - Attributes
  - HTML
  - JavaScript
  - Performance
readiness: 'Ready to Use'
standardization_status: 'W3C Proposed Recommendation'
summary: 'Provides additional control over when an external script or an HTML import is being fetched and executed while a document loads.'
uri: html/attributes/async

---
# async

## Summary

Provides additional control over when an external script or an HTML import is being fetched and executed while a document loads.

Applies to
:   [HTMLScriptElement](/dom/HTMLScriptElement)

### Declaratively Created Scripts

Usually `<script>` elements bring a browser's HTML parser to a temporary halt until the contained or referenced script has been fetched and has also been fully executed. The `async` attribute decouples script fetching and execution from the main process of HTML parsing which enables the browser to continue rendering the underlying page at full speed. A script marked with the `async` attribute will be fetched and executed at some later point in time upon which the browser is free to decide. In most cases this will be as soon as the browser finds an opportunity to request it. In addition to that such a script will also no longer respect the order in which the `<script>` elements were initially declared in the HTML source. This means that there shouldn't be other script that depend or build upon scripts marked as asynchronous. It is also important to know that the `async` attribute only works for externally referenced scripts. When attached to an inline script block this attribute is simply ignored. And finally asynchronous scripts are no longer part of the content relevant to firing the `DOMContentLoaded` event. But they are still part of the global `load` event.

### Programmatically Created Scripts

All of the above only applies to scripts declared via HTML markup. For scripts created via JavaScript the effects are sort of turned upside down. The first change is that dynamically created scripts always start off by being fully asynchronous, meaning they neither block the HTML parser nor do they respect their order of creation. The effect is the same as if one would set `script.async = true;`. What is possible here is to instead set `script.async = false;`. This won't bring the script all the way back to a point where it would block the HTML parser, but it does make the script respect the order of creation. This allows one to work with dependencies between dynamically created scripts. Beware: "order of creation" doesn't factor in any scripts declared via HTML. Declarative scripts and programmatic scripts both live, and stay, in their own worlds.

### At one glance

Characteristic
:   Declaratively w/o async
Blocking?
:   yes
In order?
:   yes

### HTML Imports

The `async` attribute appears at one other place: Attached to a `<link rel="import">` declaration. The latter denotes an HTML import, which is part of the web component eco system. Since `<link>` elements can only be placed within the `<head>` of a page and since HTML imports are usually synchronous they do have the potential to block initial page rendering a lot. Therefore it is possible to also mark such an HTML import to get handled asynchronously. The browser then does not wait on it to be finished any more before proceeding.

## Examples

The following script declaration would not block HTML parsing/rendering:

``` {.html}
<script src="script.js" async></s​cript>
```

Although not blocking it is not a good idea to mark a series of scripts that depend on each other as asynchronous:

``` {.html}
<script src="jquery.js" async></s​cript>
<script src="jquery-plugin.js" async></s​cript>
```

Instead, keep the main library synchronous and just mark those dependant on it as asynchronous:

``` {.html}
<script src="jquery.js"></s​cript>
<script src="jquery-plugin.js" async></s​cript>
```

Async attribute with programmatically created scripts:

``` {.js}
var script;

/*
 * Programmatically created scripts are always asynchronous.
 * Therefore the following results in an error:
 */

script = document.createElement("script");
script.src = "jquery.js";
document.body.appendChild(script);

script = document.createElement("script");
script.src = "jquery.plugin.js"; // Needs jQuery in place to work
document.body.appendChild(script);

/*
 * Programmatically created scripts can be told to respect
 * the order of creation, though, via async attribute.
 * So the following works:
 */

script = document.createElement("script");
script.src = "jquery.js";
script.async = false;
document.body.appendChild(script);

script = document.createElement("script");
script.src = "jquery.plugin.js"; // Needs jQuery in place to work
script.async = false;
document.body.appendChild(script);
```

Making HTML imports non-blocking:

``` {.html}
<!DOCTYPE html>
<html>
    <head>
        <link rel="import" href="component.html" async>
    </head>
    <body></body>
</html>
```

## Notes

Declaring a script to run asynchronously can improve performance by unblocking the rest of the document.

## Related specifications

Specification
:   Status
[HTML5](http://www.w3.org/TR/html5/scripting-1.html#attr-script-async)
:   W3C Proposed Recommendation
[HTML Imports](http://www.w3.org/TR/html-imports/#dfn-import-async-attribute)
:   W3C Working Draft
[Resource Priorities](https://dvcs.w3.org/hg/webperf/raw-file/tip/specs/ResourcePriorities/Overview.html#the-script-element)
:   Editor's Draft

## See also

### Other articles

-   [defer attribute](/html/attributes/defer)

### Related pages (MSDN)

-   `HTMLScriptElement`

