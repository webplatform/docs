---
title: device-width
notes:
  - 'Add description, specifications, compatibility.'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'The media feature describes the actual width of the output device, such as the entire screen width or the page sheet width.'
tags:
  - CSS
  - Media
  - Feature
uri: 'css/media queries/device-width'

---
## Summary

The media feature describes the actual width of the output device, such as the entire screen width or the page sheet width.

 On all mobile browsers, the device-width media query uses the value of screen.width. Originally, that property held the width of the screen in device pixels, but on an increasing number of mobile browser it instead holds the width of the ideal viewport (the one that you get when you use the [meta viewport tag](/tutorials/mobile_viewport)). Unfortunately it's impossible to tell which value is returned without resorting to a browser detect.

Since screen.width and the device-width media query are unreliable on mobile browsers they should not be used for responsive design purposes. Use [width](/css/media_queries/width) instead.

## Syntax

-   **device-width: \<length\>**
-   **min-device-width: \<length\>**
-   **max-device-width: \<length\>**

## Values

**\<length\>**

*Value for the width of the device must be a [length](/css/data_types/length) value and can not be negative.*

## Examples

The first media query describes a device that has a screen width of exactly 320 pixels.

The second example describes all screen devices with a screen width of 1024 pixels and higher. Note: The width of the browser does not matter in this case. Therefore you would have to use [mediaqueries: width](/css/media_queries/width).

The third media query describes all devices with a screen width not wider than 1023 pixels.

``` css
@media screen and ( device-width: 320px ) { … }

@media screen and ( min-device-width: 1024px ) { … }

@media screen and ( max-device-width: 1023px ) { … }
```

## Related specifications

[Media Queries Level 4](http://www.w3.org/TR/mediaqueries-4/)
:   Working Draft

[Media Queries](http://www.w3.org/TR/mediaqueries-4/)
:   Recommendation

