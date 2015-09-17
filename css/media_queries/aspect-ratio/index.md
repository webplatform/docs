---
title: 'aspect-ratio'
compatibility:
  feature: aspect-ratio
  topic: css
notes:
  - 'Add description, specifications, compatibility.'
readiness: 'In Progress'
summary: 'The media feature describes the aspect ratio of the output device''s rendering surface, such as the viewport aspect ratio or the aspect ratio of the page box.'
tags:
  - CSS_Media_Feature
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'css/data types/ratio'
uri: 'css/media queries/aspect-ratio'

---
## Summary

The media feature describes the aspect ratio of the output device's rendering surface, such as the viewport aspect ratio or the aspect ratio of the page box.

## Syntax

1.  **aspect-ratio: \<ratio\>**
2.  **min-aspect-ratio: \<ratio\>**
3.  **max-aspect-ratio: \<ratio\>**

## Values

**ratio**

*Value for the aspect ratio of a device's rendering surface must be a [ratio](/w/index.php?title=css/data_types/ratio&action=edit&redlink=1) value.*

## Examples

The following example describes a viewport with a minimum aspect ratio of 1. This describes all viewports, which are quadratic or have a landscape ratio. Note: The aspect ratio of the viewport must not be the same as the aspect ratio of the screen. If you want to describe the aspect ratio of the screen, you have to use [device-aspect-ratio](/css/media_queries/device-aspect-ratio).

``` html
@media screen and (min-aspect-ratio: 1/1) { ... }
```

