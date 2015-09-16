---
title: port
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'compatibility, standards, more info/cross ref to explain the concept of "port"'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Location
    href: /dom/Location
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/Location
summary: 'Sets or retrieves the port number associated with a URL.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Location/port

---
## Summary

Sets or retrieves the port number associated with a URL.

Property of [dom/Location](/dom/Location)[dom/Location](/dom/Location)

## Syntax

``` js
var port = location.port;
location.port = port;
```

## Return Value

Returns an object of type StringString

The port of the URL.

## Examples

This example function returns the **port** property of two [**a**](/html/elements/a) elements.

``` html
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
