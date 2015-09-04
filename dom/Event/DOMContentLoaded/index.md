---
title: DOMContentLoaded
tags:
  - Events
  - DOM
  - DOMEvents
readiness: 'Almost Ready'
standardization_status: 'W3C Candidate Recommendation'
notes:
  - 'Needs summary'
uri: dom/Event/DOMContentLoaded

---
# DOMContentLoaded

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

Synchronous
:   No
Bubbles
:   Yes
Target
:   dom/Document
Cancelable
:   Yes
Default action
:    ?

The **DOMContentLoaded** event fires when the markup of a webpage has been parsed, which means it also fires before the [**onload**](/dom/Element/load) event. **DOMContentLoaded** is a good place to perform initialization tasks for your webpage, such as registering event handlers, initializing handles to support objects, and so on. This allows your initialization tasks to occur while the remaining resources for the webpage are being downloaded. For more information, see the [DOMContentLoaded test drive demo.](http://go.microsoft.com/fwlink/p/?LinkId=245080)

## Examples

``` {.html}
<!doctype html>
<html>
 <head>
  <script type="text/javascript">
function logMsg( sMsg ) {
  var oLog = document.getElementById('ResultLog');
  oLog.innerText += "\n" + sMsg;
}

function addListener(obj, eventName, listener) {
    if( obj.addEventListener ) {
        obj.addEventListener( eventName, listener, false );
    } else {
        obj.attachEvent("on" + eventName, listener);
    }
}

function handleDCL( e ) {
  logMsg( "DOMContentLoaded event fired.\n" );
   var o = document.getElementById('button1');
   addListener(o, "click", handleClick1);
}

function handleClick1( e ) {
  logMsg( "Button 1 clicked.\n" );
}


if(!window.addEventListener) {
    logMsg( "Can't add eventListeners; not supported." )
} else {
   addListener(document, "DOMContentLoaded", handleDCL);
   addListener(window, "load", handleLoad);
}
  </script>
 </head>
 <body>
  <button id="button1">Click me</button>
  <div>
   <p id="ResultLog">Results appear here </p>
  </div>
 </body>
</html>
```

## Related specifications

Specification
:   Status
[HTML5](http://www.w3.org/TR/html5/single-page.html)
:   Candidate Recommendation

## See also

### Related pages (MSDN)

-   `onload`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

