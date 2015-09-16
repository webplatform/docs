---
title: 'resolution'
compatibility:
  feature: resolution
  topic: css
notes:
  - 'Add description, compatibility.'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'The media feature describes the resolution (pixel-density) of the output device. The resolution can be specified in dpi (dots per inch), dppx (dots per pixel) or dpcm (dots per centimeter).'
tags:
  - CSS
  - Media
  - Feature
uri: 'css/media queries/resolution'

---
## Summary

The media feature describes the resolution (pixel-density) of the output device. The resolution can be specified in dpi (dots per inch), dppx (dots per pixel) or dpcm (dots per centimeter).

## Syntax

1.  **resolution: \<resolution\>**
2.  **min-resolution: \<resolution\>**
3.  **max-resolution: \<resolution\>**

## Values

**resolution**

Value for the resolution of a device must be a [resolution](/css/data_types/resolution) value.

## Examples

The first media query describes a non-screen devices with a minimum resolution of 300 dots per inch.

The second example describes a device with a screen that has a pixel-density of 2 or higher.

``` css
@media print and (min-resolution: 300dpi) { ... }

@media screen and (min-resolution: 2dppx) { ... }
```

## Related specifications

[Media Queries Level 4](http://www.w3.org/TR/mediaqueries-4/)
:   Working Draft

[Media Queries](http://www.w3.org/TR/css3-mediaqueries/)
:   Recommendation

