---
title: 'Geolocation'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The Geolocation object is used by scripts to programmatically determine the location information associated with the hosting device. The location information is acquired by applying a user-agent specific algorithm, creating a Position object, and populating that object with appropriate data accordingly.'
tags:
  - API_Objects
  - API
  - Geolocation
uri: apis/geolocation/Geolocation

---
## Summary

The Geolocation object is used by scripts to programmatically determine the location information associated with the hosting device. The location information is acquired by applying a user-agent specific algorithm, creating a Position object, and populating that object with appropriate data accordingly.

## Properties

*No properties.*

## Methods

[clearWatch](/apis/geolocation/Geolocation/clearWatch)
:   Stops a specific watch process.

[getCurrentPosition](/apis/geolocation/Geolocation/getCurrentPosition)
:   Obtains the current location of the device.

[watchPosition](/apis/geolocation/Geolocation/watchPosition)
:   Returns a long value that uniquely identifies a watch operation and then asynchronously starts the watch operation.

## Events

*No events.*

## Examples

The geolocation API is published through a geolocation child object within the navigator object. If the object exists, geolocation services are available.

``` js
if ("geolocation" in navigator) {
  /* geolocation is available */
  alert("Geolocation services are supported by your browser.");
} else {
 /* geolocation is not available */
  alert("I'm sorry, but geolocation services are not supported by your browser.");
}
```

The script checks if geolocation is supported, if possible - the script obtains your actual position using the watchPosition method. If something went wrong you will get a detailed error message.

``` js
// variables
var watchID;
var geoLoc;

// check if geolocation is available
if ("geolocation" in navigator)
{
/* geolocation is available */
    alert("Geolocation services are supported by your browser.");
    getLocationUpdate();
}

else
{
/* geolocation is not available */
    alert("I'm sorry, but geolocation services are not supported by your browser.");
}

function showLocation(position)
{
alert('latitude: '+position.coords.latitude+' AND longitude: '+position.coords.longitude);
alert(position.coords.accuracy);
}

function errorHandler(err)
{
if(err.code == 0)
{alert("Error: Unknown error");}

else if( err.code == 1)
{alert("Error: Permission denied");}

else if( err.code == 2)
{alert("Error: Position not available");}

else if( err.code == 3)
{alert("Error: Timeout");}

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
```

## Notes

Windows Internet Explorer 9. The **Geolocation** object is only supported for webpages displayed in IE9 Standards mode. For more information, see Defining Document Compatibility. The **Geolocation** object is not supported for applications hosting the WebBrowser Control.

## Related specifications

[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Editor's Draft
