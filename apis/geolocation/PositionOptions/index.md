---
title: PositionOptions
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/Using_geolocation)'
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'A native script object used by the getCurrentPosition() and watchPosition() methods.'
tags:
  0: API
  1: Objects
  3: Geolocation
uri: apis/geolocation/PositionOptions

---
## <span>Summary</span>

A native script object used by the getCurrentPosition() and watchPosition() methods.

## <span>Properties</span>

API Name
:   Summary

[enableHighAccuracy](/apis/geolocation/PositionOptions/enableHighAccuracy)
:   A request from the application to receive the best possible location results. The intended purpose of this attribute is to allow applications to inform the implementation that they do not require high accuracy geolocation fixes so the implementation can avoid using geolocation providers that consume a significant amount of power (e.g., GPS).

[maximumAge](/apis/geolocation/PositionOptions/maximumAge)
:   Indicates that the application is willing to accept a cached position whose age is no greater than the specified time (in milliseconds).

[timeout](/apis/geolocation/PositionOptions/timeout)
:   Denotes the maximum length of time (expressed in milliseconds) that is allowed to pass from the call to **getCurrentPosition()** or **watchPosition()** until the corresponding **successCallback** is invoked.

## <span>Methods</span>

*No methods.*

## <span>Events</span>

*No events.*

## <span>Examples</span>

Obtain user position using high accuracy and a timeout if a location cant be found within 60 seconds.

``` js
navigator.geolocation.getCurrentPosition(geoSuccess,geoError, {'enableHighAccuracy':true,'timeout':60000,'maximumAge':0});

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

## <span>Related specifications</span>

[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Editor's Draft
