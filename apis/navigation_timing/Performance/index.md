---
title: 'Performance'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/Navigation_timing)'
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The HTML5 specification defines a Window interface, which this specification extends.'
tags:
  0: API
  1: Objects
  3: Navigation
  4: Timing
uri: 'apis/navigation timing/Performance'

---
## Summary

The HTML5 specification defines a Window interface, which this specification extends.

## Properties

API Name
:   Summary

[navigation](/apis/navigation_timing/Performance/navigation)
:   Represents the navigation information related to the browsing context. This attribute is defined by the **PerformanceNavigation** interface.

[timing](/apis/navigation_timing/Performance/timing)
:   Represents the timing information related to the browsing contexts since the last non-redirect navigation. This attribute is defined by the **PerformanceTiming** interface.

## Methods

*No methods.*

## Events

*No events.*

## Examples

The following script calculates how much time to load a page since the most recent navigation.

``` js
<html>
<head>
<script type="text/javascript">
function onLoad() {
  var now = new Date().getTime();
  var page_load_time = now - performance.timing.navigationStart;
  alert("User-perceived page loading time: " + page_load_time);
}
</script>
</head>
<body onload="onLoad()">
<!- Main page body goes from here. -->
</body>
</html>
```

## Related specifications

[W3C Navigation Timing Specification](http://w3c-test.org/webperf/specs/NavigationTiming/)
:   W3C Editor's Draft
