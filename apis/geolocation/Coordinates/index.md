---
title: 'Coordinates'
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/Using_geolocation)'
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The geographic coordinate reference system used by the attributes in this interface is the World Geodetic System (2d).'
tags:
  0: API
  1: Objects
  3: Geolocation
uri: apis/geolocation/Coordinates

---
## Summary

The geographic coordinate reference system used by the attributes in this interface is the World Geodetic System (2d).

## Properties

API Name
:   Summary

[accuracy](/apis/geolocation/Coordinates/accuracy)
:   Denotes the accuracy level of the *latitude* and *longitude* coordinates. It is specified in meters and must be supported by all implementations. The value of this attribute must be a non-negative real number.

[alititudeAccuracy](/apis/geolocation/Coordinates/alititudeAccuracy)
:   Denotes the accuracy level of the *altitude* coordinate, specified in meters. If the implementation cannot provide altitude information, the value of this attribute must be null.

[altitude](/apis/geolocation/Coordinates/altitude)
:   Denotes the height of the position, specified in meters above the ellipsoid. If the implementation cannot provide altitude information, the value of this attribute must be null.

[heading](/apis/geolocation/Coordinates/heading)
:   Denotes the direction of travel of the hosting device specified in degrees, where 0° ≤ heading \< 360°, counting clockwise relative to the true north. If the implementation cannot provide heading information, the value of this attribute must be null. If the hosting device is stationary (i.e., the value of the *speed* attribute is 0), then the value of this attribute must be NaN.

[latitude](/apis/geolocation/Coordinates/latitude)
:   Geographic latitude specified in decimal degrees.

[longitude](/apis/geolocation/Coordinates/longitude)
:   Geographic longitude specified in decimal degrees.

[speed](/apis/geolocation/Coordinates/speed)
:   Denotes the magnitude of the horizontal component of the hosting device's current velocity specified in meters per second. If the implementation cannot provide speed information, the value of this attribute must be null. Otherwise, the value of this attribute must be a non-negative real number.

## Methods

*No methods.*

## Events

*No events.*

## Examples

Obtain user location with all available information available within to coordinates object.

``` js
navigator.geolocation.getCurrentPosition(geoSuccess,geoError);

/* Position found*/
function geoSuccess(position)
{
alert('latitude: '+position.coords.latitude+' AND longitude: '+position.coords.longitude);
/* Denotes the accuracy level of the latitude and longitude coordinates in meters */
alert(position.coords.accuracy);
/* Denotes the accuracy level of the altitude coordinate in meters */
alert(position.coords.alititudeAccuracy);
/* Denotes the height of the position, specified in meters above the ellipsoid. */
alert(position.coords.altitude);
/* Denotes the direction of travel of the hosting device specified in degrees */
alert(position.coords.heading);
/* Denotes the magnitude of the horizontal component of the hosting device's current velocity specified in meters per second. */
alert(position.coords.speed);
}

/* Position not found*/
function geoError(position)
{
alert("No position found");
}
```

## Related specifications

[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Proposed Recommendation
