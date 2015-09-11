---
title: device-aspect-ratio
notes:
  - 'Add description, specifications, compatibility.'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'The media feature describes the actual aspect ratio of the output device, such as the aspect ratio of an entire screen or the aspect ratio of a page sheet.'
tags:
  - CSS
  - Media
  - Feature
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'css/data types/ratio'
uri: 'css/media queries/device-aspect-ratio'

---
## <span>Summary</span>

The media feature describes the actual aspect ratio of the output device, such as the aspect ratio of an entire screen or the aspect ratio of a page sheet.

### <span>Syntax</span>

**device-aspect-ratio: \<ratio\>**

### <span>Values</span>

**ratio**

*Value for the aspect ratio of a device's rendering surface must be a [ratio](/w/index.php?title=css/data_types/ratio&action=edit&redlink=1) value.*

## <span>Examples</span>

The example describes all screen devices with a screen aspect ratio of 16:9 or smaller and therefore all widescreens that are 16:9 or wider. Note: The flexible aspect ratio of the browser or any other rendering surface does not matter in this case. Therefore you would have to use [mediaqueries: aspec-ratio](/css/media_queries/width).

``` css
@media screen and ( max-device-aspect-ratio: 16/9 ) { … }
```

## <span>Related specifications</span>

[Media Queries Level 4](http://www.w3.org/TR/mediaqueries-4/)
:   Working Draft

[Media Queries](http://www.w3.org/TR/css3-mediaqueries/)
:   Recommendation

