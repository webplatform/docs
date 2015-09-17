---
title: 'getTimezoneOffset'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/014ykh71(v=vs.94).aspx)'
compatibility:
  feature: getTimezoneOffset
  topic: javascript
readiness: 'Ready to Use'
summary: 'Gets the difference in minutes between the time on the local computer and Universal Coordinated Time (UTC).'
tags:
  - JS_Basic
  - JS_Method
uri: javascript/Date/getTimezoneOffset

---
## Summary

Gets the difference in minutes between the time on the local computer and Universal Coordinated Time (UTC).

## Syntax

    dateObj.getTimezoneOffset()

## Return Value

Returns the number of minutes between the time on the current computer (either the client machine or, if this method is called from a server script, the server machine) and UTC. It is positive if the current computer's local time is behind UTC (e.g., Pacific Daylight Time), and negative if the current computer's local time is ahead of UTC (e.g., Japan). If a server in New York City is contacted by a client in Los Angeles on December 1, **getTimezoneOffset** returns 480 if executed on the client, or 300 if executed on the server.

## Examples

The following example shows how to use the **getTimezoneOffset** method.

``` js
var date =  new Date();
 var minutes = date.getTimezoneOffset();

 if (minutes < 0)
     document.write(minutes / 60 + " hours after UTC");
 else
     document.write(minutes / 60 + " hours before UTC");

 // Output (for example, where local time is PST):
 7 hours before UTC
```

## Remarks

The required dateObj reference is a **Date** object.

## See also

### Other articles

-   [getTime Method (Date)](/javascript/Date/getTime)

