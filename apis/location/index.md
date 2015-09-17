---
title: 'window.location'
readiness: 'Ready to Use'
summary: 'The location object provides access to the address related properties of the current document.'
tags:
  - API_Objects
  - JavaScript
uri: apis/location

---
## Summary

The location object provides access to the address related properties of the current document.

## Properties

[hash](/apis/location/hash)
:   The hash property contains the fragment identifier (including hash character) for the current page.

[host](/apis/location/host)
:   The host property contains the host part of the the current document URL, (hostname:port).

[hostname](/apis/location/hostname)
:   The hostname property contains the hostname the current document was served from, excluding protocol, port, and other information.

[href](/apis/location/href)
:   The full url for this resource. Synonymous with `String(window.location)`.

[pathname](/apis/location/pathname)
:   The path to the current document, relative to the root of the current host.

[port](/apis/location/port)
:   The port number the document was accessed via.

[protocol](/apis/location/protocol)
:   Sets or retrieves the protocol portion of a URL.

    The protocol the current document was accessed via (everything preceding the "//").

[search](/apis/location/search)
:   The search property contains the query string portion of the current url.

## Methods

[assign](/apis/location/assign)
:   Navigate to a new page.

[reload](/apis/location/reload)
:   Refresh/reload the current page, optionally forcing a re-download of the content.

[replace](/apis/location/replace)
:   Similar to `window.location.assign`, except that it "replaces" the current document, removing the previous one from the back button history.

## Events

*No events.*

## Examples

Redirect the current page to example.org.

``` js
window.location = "http://example.org";
```

Show an alert if the current page is example.org.

``` html
if(window.location == "http://example.org/"){
    alert("Welcome to example.org!");
}
```

## Usage

     The location object can be used as an object or a string.

Regular string comparisons such as in the examples section can be used, but there are several other properties of the location such as the hash or the hostname that can be compared individually.
