---
title: 'height'
compatibility:
  feature: height
  topic: css
notes:
  - 'Add description, compatibility.'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'The media feature describes the height of the output device''s rendering surface, such as the viewport height or the height of the page box.'
tags:
  - CSS_Media_Feature
uri: 'css/media queries/height'

---
## Summary

The media feature describes the height of the output device's rendering surface, such as the viewport height or the height of the page box.

## Description

Just as the [width media query](/css/media_queries/width) reports the layout viewport's width, the height media query reports its height. It tells you how many CSS pixels are available vertically for showing content, which is occasionally useful if you need to figure out if an item will be shown "above the fold."

Although the layout viewport width (and thus the media query) is equal to the width of the html element, this does \*not\* hold for height. Frequently, the html element's height is a lot larger than the layout viewport height. The height media query's value is usually the width media query value divided by the screen's aspect ratio.

The height media query is always equal to document.documentElement.clientHeight.

One serious problem on many mobile browsers is that the layout viewport height, and thus the height media query value, changes when the browser toolbar moves into or out of view. Thus, a height media query that works perfectly when the page is scrolled up and the toolbar is visible, may misfire when the user scrolls, the toolbar moves out of view, and the layout viewport height changes.

For this reason it's best to use height media queries sparingly, and, if you need them, to give browsers ample leeway. In general you should expect a browser toolbar to be between 40 and 70 pixels high.

## Syntax

-   **height: \<length\>**
-   **min-height: \<length\>**
-   **max-height: \<length\>**

## Values

**\<length\>**

*Value for the height of the device's viewport must be a [length](/css/data_types/length) value and can not be negative.*

## Examples

The first media query describes a viewport with a height of exactly 480 pixels. Note: The height of the viewport, for example in a smartphone browser is not the same as the height of the screen, because of the browser bars. If you want to describe the screen height, you have to use [mediaqueries: device-height](/css/media_queries/device-height).

The second example describes viewports with height of 700 pixels and higher.

The third media query describes all viewports with a height not bigger than 699 pixels.

``` css
@media screen and ( height: 400px ) { … }

@media screen and ( min-height: 700px ) { … }

@media screen and ( max-height: 699px ) { … }
```

## Related specifications

[Media Queries Level 4](http://www.w3.org/TR/mediaqueries-4/)
:   Working Draft

[Media Queries](http://www.w3.org/TR/css3-mediaqueries/)
:   Recommendation

