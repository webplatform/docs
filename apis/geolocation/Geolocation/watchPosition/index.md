---
title: watchPosition
tags:
  0: API
  1: Object
  2: Methods
  4: Geolocation
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns a long value that uniquely identifies a watch operation and then asynchronously starts the watch operation.'
uri: apis/geolocation/Geolocation/watchPosition

---
# watchPosition

## Summary

Returns a long value that uniquely identifies a watch operation and then asynchronously starts the watch operation.

*Method of [apis/geolocation/Geolocation](/apis/geolocation/Geolocation)*

## Syntax

``` {.js}
var object = Geolocation.watchPosition(successCallback, errorCallback, options);
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

The function to call when the attempt to obtain geographic position fails. The function specified by the *errorCallback* parameter takes one *positionError* parameter. To use the *options* parameter without using the *errorCallback* parameter, specify a **null** value for the *errorCallback* parameter.

### options

 Data-typeÂ
:   any

*(Optional)*

JSON encoding

## Return Value

Returns an object of type unsigned long.

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

Obtains users position and position changes for 120s.

``` {.js}
var watchID;
var geoLoc;

function showLocation(position)
{
alert('latitude: '+position.coords.latitude+' AND longitude: '+position.coords.longitude);
}

function errorHandler(err) {
  if(err.code == 1) {
    alert("Error: Access is denied!");
  }else if( err.code == 2) {
    alert("Error: Position is unavailable!");
  }
}
function getLocationUpdate(){

   if(navigator.geolocation){
      // timeout at 120000 milliseconds (120 seconds)
      var options = {timeout:120000};
      geoLoc = navigator.geolocation;
      watchID = geoLoc.watchPosition(showLocation,
                                     errorHandler,
                                     options);
   }else{
      alert("Sorry, browser does not support geolocation!");
   }
}
getLocationUpdate();
```

## Notes

The function begins acquiring the geographic position and returns immediately. When the position is successfully obtained, the callback function provided in the *successCallback* parameter is called. The parameter to the *successCallback* function is a **position** object that contains the data on the current geographic location. If the attempt to obtain the user's location fails, the callback function that can be provided as an optional second parameter is called. The error parameter to the *errorCallback* function is a **positionError** object that contains an error code indicating the reason for failure.

**Note:**Â Â The first time a document calls the **watchPosition** function, the client requests permission to access the geographic location of the browser, unless the user has previously chosen to always allow or always deny permission for the website to determine location. If the user denies permission, the function declared by the *errorCallback* is called and the code attribute of the error parameter of that function is set to PositionError.PERMISSION\_DENIED. Support for the attributes of the *options* parameter depends on the location provider available to the device running the client. There is no guarantee that changing the properties of these attributes will affect the results reported by the location provider. Windows Internet ExplorerÂ 9. This property is supported only for webpages displayed in IE9 Standards mode. For more information, please see Defining Document Compatibility.

## Related specifications

Specification
:   Status
[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources, including ones licensed under the CC-BY-SA license.* [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)

Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/Using_geolocation)

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

