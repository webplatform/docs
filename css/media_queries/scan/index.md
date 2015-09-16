---
title: scan
notes:
  - 'Add summary, values, syntax, examples, description, compatibility.'
readiness: 'Not Ready'
standardization_status: 'W3C Recommendation'
summary: "The scan media feature describes the scanning process (i.e. how the video card generates the image) of some output devices. \n"
tags:
  - CSS
  - Media
  - Feature
uri: 'css/media queries/scan'

---
## Summary

The scan media feature describes the scanning process (i.e. how the video card generates the image) of some output devices.

It can be useful if you want to adjust font type that are known to not be visible well on "interlaced" modes for instance.

**Needs Examples**: This section should include examples.

## Usage

     @media (scan: interlace) { body { font-family: sans-serif; } }

## Related specifications

[Media Queries Level 4](http://www.w3.org/TR/mediaqueries-4/)
:   Working Draft

[Media Queries](http://www.w3.org/TR/css3-mediaqueries/)
:   Recommendation

## See also

### External resources

-   [CSS Working Group Draft](http://dev.w3.org/csswg/mediaqueries-4/#descdef-media-scan)
