---
title: 'creationTime'
notes:
  - 'Needs example, spec reference'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/media_source_extensions/VideoPlaybackQuality
    href: /apis/media_source_extensions/VideoPlaybackQuality
  return:
    predicate: 'Returns an object of type '
    value: VARIANT
    href: /apis/media_source_extensions/VideoPlaybackQuality
standardization_status: 'W3C Editor''s Draft'
summary: 'Gets the timestamp for when the VideoPlaybackQuality metrics were collected.'
tags:
  - API_Object_Properties
  - Needs_Examples
uri: 'apis/media source extensions/VideoPlaybackQuality/creationTime'

---
## Summary

Gets the timestamp for when the VideoPlaybackQuality metrics were collected.

Property of [apis/media\_source\_extensions/VideoPlaybackQuality](/apis/media_source_extensions/VideoPlaybackQuality)[apis/media\_source\_extensions/VideoPlaybackQuality](/apis/media_source_extensions/VideoPlaybackQuality)

## Syntax

``` js
var time = VideoPlaybackQuality.creationTime;
VideoPlaybackQuality.creationTime = time;
```

## Return Value

Returns an object of type VARIANTVARIANT

Type: DOMHighResTimeStamp The timestamp for when the quality metrics were collected.

