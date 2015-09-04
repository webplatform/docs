---
title: port
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
notes:
  - 'compatibility, standards, more info/cross ref to explain the concept of "port"'
summary: 'Sets or retrieves the port number associated with a URL.'
uri: dom/Location/port

---
# port

## Summary

Sets or retrieves the port number associated with a URL.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Location](/dom/Location)</span></span>

## Syntax

``` {.js}
var port = location.port;
location.port = port;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The port of the URL.

## Examples

This example function returns the **port** property of two [**a**](/html/elements/a) elements.

``` {.html}
<script>
function getPort()
{
    console.log("FTP: " + document.getElementById("ftp").port + "\n" + "HTTP: " + document.getElementById("http").port);
}
</script>

<a href="ftp://www.microsoft.com" onclick="getPort();" id="ftp">ftp</a>
<a href="http://www.microsoft.com" onclick="getPort();" id="http">http</a>
```

## Notes

The port will resolve based on the default port for the protocol set in the HREF attribute: `21` for FTP, `80` for HTTP, and so forth. Proprietary protocols that do not require a port return `0` or an empty string. [**location**](/dom/Location).**port** returns an empty string when read in a page reached by the http protocol.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

