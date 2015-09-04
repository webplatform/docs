---
title: Performance
tags:
  0: API
  1: Objects
  3: Resource
  4: Timing
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Provides methods for performance timing.'
uri: 'apis/resource timing/Performance'

---
# Performance

## Summary

Provides methods for performance timing.

## Properties

API Name
:   Summary
[onresourcetimingbufferfull](/apis/resource_timing/Performance/onresourcetimingbufferfull)
:   This callback is triggered when the buffer used to store the list of PerformanceResourceTiming is full.

## Methods

API Name
:   Summary
[clearResourceTimings](/apis/resource_timing/Performance/clearResourceTimings)
:   Clears the buffer used to store the current list of PerformanceResourceTiming resources.
[setResourceTimingBufferSize](/apis/resource_timing/Performance/setResourceTimingBufferSize)
:   Sets the maximum number of PerformanceResourceTiming resources that may be stored in the buffer to the value of the maxSize parameter.

## Events

*No events.*

## Examples

The following script calculates the amount of time it takes to fetch every resource in the page, even those defined in markup:

    <!doctype html>
    <html>
      <head>
      </head>
      <body onload="loadResources()">
        <script>
           function loadResources()
           {
              var image1 = new Image();
              image1.src = 'http://w3c-test.org/webperf/image1.png';
              image1.onload = resourceTiming;
           }

           function resourceTiming()
           {
               var resourceList = window.performance.getEntriesByType("resource");
               for (i = 0; i < resourceList.length; i++)
               {
                  if (resourceList[i].initiatorType == "img")
                  {
                     alert("End to end resource fetch: "+ resourceList[i].responseEnd - resourceList[i].startTime);
                  }
               }
           }
        </script>
        <img id="image0" src="http://w3c-test.org/webperf/image0.png">
      </body>
    </html>

## Related specifications

Specification
:   Status
[W3C Resource Timing Specification](http://www.w3.org/TR/resource-timing/#extensions-performance-interface)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

