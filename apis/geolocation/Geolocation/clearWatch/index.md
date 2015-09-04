---
title: clearWatch
tags:
  0: API
  1: Object
  2: Methods
  4: Geolocation
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Stops a specific watch process.'
uri: apis/geolocation/Geolocation/clearWatch

---
# clearWatch

## Summary

Stops a specific watch process.

*Method of [apis/geolocation/Geolocation](/apis/geolocation/Geolocation)*

## Syntax

``` {.js}
 Geolocation.clearWatch(watchId);
```

## Parameters

### watchId

 Data-typeÂ
:   unsigned long

 The ID of the watch operation to cancel. This value is returned by the **watchPosition** method.

## Return Value

No return value

## Examples

``` {.js}
geoLoc = navigator.geolocation;
watchID = geoLoc.watchPosition(successCallback, errorHandler, options);
geoLoc.clearWatch(watchID);
```

## Notes

If the *watchId* parameter does not correspond to any watch process started by a previous call to the **watchPosition** method, this method returns and no further action is taken. Otherwise, the watch process identified by *watchId* is immediately stopped and no further callbacks must be invoked.

## Related specifications

Specification
:   Status
[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

