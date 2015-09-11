---
title: PositionError
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/Using_geolocation)'
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The container for Position error information returned by this API.'
tags:
  0: API
  1: Objects
  3: Geolocation
uri: apis/geolocation/PositionError

---
## <span>Summary</span>

The container for Position error information returned by this API.

## <span>Properties</span>

API Name
:   Summary

[code](/apis/geolocation/PositionError/code)
:   The error code of the current PositionError.

[message](/apis/geolocation/PositionError/message)
:   The error text of the current PositionError, describing the details of the error encountered. This attribute is primarily intended for debugging and developers should not use it directly in their application user interface.

## <span>Methods</span>

*No methods.*

## <span>Events</span>

*No events.*

## <span>Examples</span>

Displays error with detailed information.

``` js
navigator.geolocation.getCurrentPosition(geoSuccess,geoError);

/* Position found*/
function geoSuccess(position)
{
alert("Position found.");
}

/* Position not found*/
function geoError(err)
{
if(err.code == 0)
{alert("Error: Unknown error");}

else if( err.code == 2)
{alert("Error: Permission denied");}

else if( err.code == 2)
{alert("Error: Position not available");}

else if( err.code == 3)
{alert("Error: Timeout");}

else
{alert(err.message);}
}
```

## <span>Related specifications</span>

[W3C Geolocation Specification](http://dev.w3.org/geo/api/spec-source.html)
:   W3C Editor's Draft
