---
title: 'Vibration API'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The Vibration API provides access to the vibration mechanism of the hosting device. Vibration is a form of tactile feedback, often used by mobile phones.'
tags:
  0: API
  1: Listings
  3: Mobile
  4: Vibration
uri: apis/vibration

---
## Summary

The Vibration API provides access to the vibration mechanism of the hosting device. Vibration is a form of tactile feedback, often used by mobile phones.

## Usage

     This API is specifically designed to address use cases that require simple tactile feedback only. This API is not meant to be used as a generic notification mechanism. Such use cases may be handled using the Web Notifications specification.

In the following example the device will vibrate for 1000 milliseconds (ms):

``` js
navigator.vibrate(1000);
// or alternatively
navigator.vibrate([1000]);
```

 In the following example the pattern will cause the device to vibrate for 50 ms, be still for 100 ms, and then vibrate for 150 ms:

``` js
navigator.vibrate([50, 100, 150]);
```

 The following example cancels any existing vibrations:

``` js
navigator.vibrate(0);
// or alternatively
navigator.vibrate([]);
```

## See also

### Related articles

#### Mobile

-   [Battery Status API](/apis/battery_status)

-   [Mediastream Image Capture](/apis/image_capture)

-   [Media Capture and Streams](/apis/media_capture_and_streams)

-   [Network Information API](/apis/network_information)

-   **Vibration API**

-   [capture](/html/attributes/capture)

### External resources

-   [Vibration API](http://www.w3.org/TR/vibration/)
-   [Vibration API - W3C Candidate Recommendation 23 July 2013](http://www.w3.org/TR/2013/CR-vibration-20130723/)
-   [Device APIs working group](http://www.w3.org/2009/dap/)
