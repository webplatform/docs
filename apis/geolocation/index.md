---
title: 'Geolocation API'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The geolocation API lets you share your location with trusted web sites. The latitude and longitude are available to JavaScript on the page, which in turn can send it back to the remote web server and do fancy location-aware things like finding local businesses or showing your location on a map.'
tags:
  - API_Listings
  - API
  - Geolocation
uri: apis/geolocation

---
## Summary

The geolocation API lets you share your location with trusted web sites. The latitude and longitude are available to JavaScript on the page, which in turn can send it back to the remote web server and do fancy location-aware things like finding local businesses or showing your location on a map.

[Coordinates](/apis/geolocation/Coordinates)
:   The geographic coordinate reference system used by the attributes in this interface is the World Geodetic System (2d).

[Geolocation](/apis/geolocation/Geolocation)
:   The Geolocation object is used by scripts to programmatically determine the location information associated with the hosting device. The location information is acquired by applying a user-agent specific algorithm, creating a **Position** object, and populating that object with appropriate data accordingly.

[PositionError](/apis/geolocation/PositionError)
:   The container for Position error information returned by this API.

[PositionOptions](/apis/geolocation/PositionOptions)
:   A native script object used by the **getCurrentPosition()** and **watchPosition()** methods.
