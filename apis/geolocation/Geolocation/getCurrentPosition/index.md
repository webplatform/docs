---
title: getCurrentPosition
tags:
  0: API
  1: Object
  2: Methods
  4: Geolocation
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Obtains the current location of the device.'
uri: apis/geolocation/Geolocation/getCurrentPosition

---
# getCurrentPosition

## Summary

Obtains the current location of the device.

*Method of [apis/geolocation/Geolocation](/apis/geolocation/Geolocation)*

## Syntax

``` {.js}
 Geolocation.getCurrentPosition(successCallback, errorCallback, options);
```

## Parameters

### successCallback

 Data-typeÂ
:   any

 The function to call when geographic position is successfully obtained. The function specified by the *successCallback* parameter takes one *position* parameter.

### errorCallback

 Data-typeÂ
:   any

*(Optional)*

The function to call when the method fails. The function specified by the *errorCallback* parameter takes one *positionError* parameter. To use the *options* parameter without using the *errorCallback* parameter, set the *errorCallback* parameter to **null**.

### options

 Data-typeÂ
:   any

*(Optional)*

JSON encoding

## Return Value

No return value

## Examples

Obtains user current position.

``` {.js}
navigator.geolocation.getCurrentPosition(geoSuccess,geoError);

/* Position found*/
function geoSuccess(position)
{
alert('latitude: '+position.coords.latitude+' AND longitude: '+position.coords.longitude);
}

/* Position not found*/
function geoError(position)
{
alert("No position found");
}
```

## Notes

Windows Internet ExplorerÂ 9. This property is supported only for webpages displayed in IE9 Standards mode. For more information, see Defining Document Compatibility. When the **getCurrentPosition** function is called, it initiates a request to acquire the geographic position, and then returns immediately. If the geographic position is successfully obtained, the callback function defined in the *successCallback* parameter is called. The *position* parameter of that function contains the data describing the current geographic location of the device running Internet Explorer. If the geographic location cannot be obtained and a callback function is specified as the *errorCallback* parameter, that function is called. The error parameter of the *errorCallback* function contains an error code indicating the reason for failure.

**Note:**Â Â The first time a web application calls the **getCurrentPosition** function, Internet Explorer requests permission to access the geographic location of the browser, unless the user has previously chosen to always allow or always deny permission for the website to determine location. If the user denies permission, the function declared by the *errorCallback* is called, and the code attribute of the error parameter of that function is set to PositionError.PERMISSION\_DENIED. Support for the attributes of the *options* parameter depends on the location provider available to the device running Internet Explorer. There is no guarantee that changing the properties of these attributes will affect the results reported by the location provider.

## Related specifications

Specification
:   Status
[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources, including ones licensed under the CC-BY-SA license.* [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)

Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/Using_geolocation)

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

