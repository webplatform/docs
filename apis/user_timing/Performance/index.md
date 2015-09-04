---
title: Performance
tags:
  0: API
  1: Objects
  3: User
  4: Timing
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Exposes a high precision timestamp to developers so they can better measure the performance of their applications.'
uri: 'apis/user timing/Performance'

---
# Performance

## Summary

Exposes a high precision timestamp to developers so they can better measure the performance of their applications.

## Properties

*No properties.*

## Methods

API Name
:   Summary
[clearMarks](/apis/user_timing/Performance/clearMarks)
:   Removes all DOMHighResTimeStamp time values for the given mark name, or removes all marks and their associated DOMHighResTimeStamp time values.
[clearMeasures](/apis/user_timing/Performance/clearMeasures)
:   Removes all DOMHighResTimeStamp durations for the given measure name, or removes all measures and their associated DOMHighResTimeStamp durations.
[mark](/apis/user_timing/Performance/mark)
:   Stores a timestamp with the associated name (a "mark").
[measure](/apis/user_timing/Performance/measure)
:   Stores the DOMHighResTimeStamp duration between two marks along with the associated name (a "measure").

## Events

*No events.*

## Examples

The following script shows how a developer can use the interfaces defined in this document to obtain timing data related to developer scripts.

``` {.js}
<!doctype html>
<html>
  <head>
    <title>User Timing example</title>
  </head>
  <body onload="init()">
    <script>
       function init()
       {
            performance.mark("startTask1");
            doTask1(); // Some developer code
            performance.mark("endTask1");

            performance.mark("startTask2");
            doTask2(); // Some developer code
            performance.mark("endTask2");

            measurePerf();
       }

       function measurePerf()
       {
           var perfEntries = performance.getEntriesByType("mark");
           for (var i = 0; i < perfEntries.length; i++)
           {
                 if (window.console) console.log("Name: "        + perfEntries[i].name      +
                                                 " Entry Type: " + perfEntries[i].entryType +
                                                 " Start Time: " + perfEntries[i].startTime +
                                                 " Duration: "   + perfEntries[i].duration  + "\n");
           }
       }
    </script>
  </body>
</html>
```

## Related specifications

Specification
:   Status
[W3C User Timing Specification](http://www.w3.org/TR/user-timing/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

