---
title: <resolution>
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/Web/CSS/resolution)'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The &lt;resolution&gt; CSS data type, used in media queries, denotes the granularity or possible fineness of detail of an output device. It is expressed as a &lt;number&gt; immediately followed by a unit of resolution (dpi, dpcm, ...). Like for any CSS dimension, there is no space between the number and the unit abbreviation.'
tags:
  - Data
  - Type
  - CSS
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'css/property/image resolution'
uri: 'css/data types/resolution'

---
## <span>Summary</span>

The &lt;resolution&gt; CSS data type, used in media queries, denotes the granularity or possible fineness of detail of an output device. It is expressed as a &lt;number&gt; immediately followed by a unit of resolution (dpi, dpcm, ...). Like for any CSS dimension, there is no space between the number and the unit abbreviation.

 The resolution value specifies the display or print dot density per unit of distance. A "dot" is the finest level of detail that the device can display, such as a physical screen pixel or a dot of printed ink.

On screens, the resolution is calculated relative to CSS inches, centimeters or pixels, not to physical values. For media queries, if the resolution is different in the horizontal and vertical directions *both* values must match the media query.

Unlike the CSS [**\<length\>** data type](/css/data_types/length), the unit may not be omitted for the value **0**: specifying a resolution of **0** is invalid and does not represent **0dpi**, **0dpcm**, nor **0dppx**.

## <span>Units</span>

**dpi**
:   This unit represents the number of dots per inch. A screen typically contains 72 or 96 dpi; a printed document usually reach much greater dpi. As 1 inch is 2.54 cm, **1dpi ≈ 2.54dpcm**.
**dpcm**
:   This unit represents the number of dots per centimeter. As 1 inch is 2.54 cm, **1dpcm ≈ 0.39dpi**.
**dppx**
:   This unit represents the number of dots per px unit. Due to the 1:96 fixed ratio of CSS **in** to CSS **px**, **1dppx** is equivalent to **96dpi**, that corresponds to the default resolution of images displayed in CSS as defined by the [image-resolution](/w/index.php?title=css/property/image_resolution&action=edit&redlink=1) property.

## <span>Examples</span>

Here are some correct uses of \<resolution\> values:

``` css
/* Correct use: a <number> (here an <integer>) followed by the unit. */
96dpi

/* Correct use in the context of a media query. */
@media print and (min-resolution: 300dpi) { ... }
```

Here are some incorrect uses:

``` css
/* Incorrect: no spaces allowed between the <number> and the unit. */
72 dpi

/* Incorrect: only digits must be used. */
ten dpi

/* Incorrect: the unit can be omitted for 0 values only for <length>. */
0
```

## <span>Related specifications</span>

[CSS Values and Units Module Level 3](http://www.w3.org/TR/css3-values/)
:   Candidate Recommendation

[CSS Image Values and Replaced Content Module Level 3](http://dev.w3.org/csswg/css3-images/#resolution-units)
:   Candidate Recommendation

[Media Queries](http://dev.w3.org/csswg/css3-mediaqueries/#resolution)
:   Recommendation

## <span>See also</span>

### <span>Related articles</span>

#### <span>Media Queries</span>

-   [Responsive Web Design](/concepts/mobile_web/responsive_design)

-   **\<resolution\>**

-   [accelerator](/css/media_queries/accelerator)

-   [MediaQueryList](/css/media_queries/apis/MediaQueryList)

-   [MediaQueryListListener](/css/media_queries/apis/MediaQueryListListener)

-   [StyleMedia](/css/media_queries/apis/StyleMedia)

-   [addListener](/css/media_queries/apis/addListener)

-   [handleChange](/css/media_queries/apis/handleChange)

-   [matchMedia](/css/media_queries/apis/matchMedia)

-   [matchMedium](/css/media_queries/apis/matchMedium)

-   [matches](/css/media_queries/apis/matches)

-   [media](/css/media_queries/apis/media)

-   [type](/css/media_queries/apis/properties/type)

-   [removeListener](/css/media_queries/apis/removeListener)

-   [Colors by](/css/media_queries/colors_by)

-   [device-height](/css/media_queries/device-height)

-   [filter](/css/media_queries/filter)

-   [ms-interpolation-mode](/css/media_queries/ms-interpolation-mode)

-   [behavior](/css/properties/behavior)
