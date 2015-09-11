---
title: mediaqueries
tags:
  - CSS
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'media features'
uri: css/mediaqueries

---
## <span>Introduction</span>

Media Queries are a paradigm [with origins in CSS2 Media Types](http://www.w3.org/TR/CSS2/media.html) which were then [enhanced in CSS3](http://www.w3.org/TR/css3-mediaqueries/) with the introduction of Media Features. By combining media types and media features into a media query, a developer is able to apply styles only when certain conditions are met, such as the viewing device being of media type *screen* or when the current viewport is below or above a certain height or width threshold. This allows for both subtle and drastic changes in layout and appearance of a website all controlled entirely within the site's CSS.

## <span>Syntax</span>

Media queries consist of a media type and can, as of the CSS3 specification, contain one or more media feature expressions, which will resolve to either true or false. The result of the query is true if the media type specified in the media query matches the type of device the document is being displayed with **and** all media feature expressions are true.

When a media query is true, the corresponding style sheet or style rules are applied. Selectors inside active media queries are placed into the normal cascade and do not automatically have higher precedence than those outside of active media queries. Style sheets with media queries attached to their *\<link\>* tags [will still download](http://scottjehl.github.com/CSS-Download-Tests/) even if their media queries would return false (they will not apply, however).

Unless using the *not* or *only* operators, the media type is optional and the *all* type will be implied.

### <span>Logical Operators</span>

You can compose complex media queries using logical operators, including *not*, *and*, and *only*. The *and* operator is used for combining multiple [media features](/w/index.php?title=media_features&action=edit&redlink=1) together into a single media query, requiring each chained feature to return true in order for the query to be true. The *not* operator is used to negate an entire media query. The *only* operator is used to apply a style only if the entire query matches, useful for preventing older browsers from applying selected styles. Both the *not* and the *only* operators require a media type in order to be evaluated, *all* is not implied.

In addition, you can combine multiple media queries in a comma-separated list; if any of the media queries in the list is true, the entire media statement returns true. This is equilivant to an *or* operator.

#### <span>and</span>

The *and* keyword is used for combining multiple media features together, as well as combining media features with media types. A basic media query, a single media feature with the implied *all* media type, could look like this:

||
|@media (min-width: 700px) { ... }|

If, however, you wanted this to apply only if the display is in landscape, you could use an *and* operator to chain the media features together.

||
|@media (min-width: 700px) and (orientation: landscape) { ... }|

Now the above media query will only return true if the viewport is 700px wide or wider and the display is in landscape. If, however, you only wanted this to apply if the display in question was of the media type TV, you could chain these features with a media type using an *and* operator.

||
|@media tv and (min-width: 700px) and (orientation: landscape) { ... }|

Now, the above media query will only apply if the media type is TV, the viewport is 700px wide or wider, and the display is in landscape.

#### <span>comma-separated lists</span>

Comma-separated lists behave like the logical operator *or* when used in media queries. When using a comma-separated list of media queries, if any of the media queries returns true, the styles or style sheets get applied. Each media query in a comma-separated list is treated as an individual query, and any operator applied to one media query does not affect the others. This means the comma-separated media queries can target different media features, types, and states.

For instance, if you wanted to apply a set of styles if the viewing device either had a minimum width of 700px or was a handheld in landscape, you could write the following:

||
|@media (min-width: 700px), handheld and (orientation: landscape) { ... }|

Above, if I were on a *screen* device with a viewport width of 800px, the media statement would return true because the first part, interperated as *@media all and (min-width: 700px)* would apply to my device and therefore return true, despite the fact that my *screen* device would fail the *handheld* media type check in the second media query. Likewise, if I were on a *handheld* device held in landscape with a viewport width of 500px, while the first media query would fail due to the viewport width, the second media query would succeed and thus the media statement would return true.

#### <span>not</span>

The *not* keyword applies to the whole media query and returns true if the media query would otherwise return false (such as *monochrome* on a color display or a screen width of 600px with a *min-width: 700px* feature query). A *not* will only negate the media query it is applied to and not to every media query if present in a comma-separated list of media queries. The *not* keyword cannot be used to negate an individual feature query, only an entire media query. For example, the *not* is evaluated last in the following query:

||
|@media not all and (monochrome) { ... }|

This means that the query is evaluated like this:

||
|@media not (all and (monochrome)) { ... }|

... rather than like this:

||
|@media (not all) and (monochrome) { ... }|

As another example, look at the following media query:

||
|@media not screen and (color), print and (color)|

It is evaluated like this:

||
|@media (not (screen and (color))), print and (color)|

#### <span>only</span>

The *only* keyword prevents older browsers that do not support media queries with media features from applying the given styles:

||
|\<link rel="stylesheet" media="only screen and (color)" href="example.css" /\>|

## <span>Media features</span>

-   [any-hover](/css/media_queries/any-hover)
-   [any-pointer](/css/media_queries/any-pointer)
-   [[css/media queries/aspect-ratio|aspect-ratio]\*[color](/css/media_queries/color)
-   [color-index](/css/media_queries/color-index)
-   [device-aspect-ratio](/css/media_queries/device-aspect-ratio)
-   [device-height](/css/media_queries/device-height)
-   [device-width](/css/media_queries/device-width)
-   [grid](/css/media_queries/grid)
-   [height](/css/media_queries/height)
-   [monochrome](/css/media_queries/monochrome)
-   [orientation](/css/media_queries/orientation)
-   [resolution](/css/media_queries/resolution)
-   [scan](/css/media_queries/scan)
-   [view-mode](/css/media_queries/view-mode)
-   [width](/css/media_queries/width)

## <span>See also</span>

-   [Media Queries Specification](http://www.w3.org/TR/css3-mediaqueries/)
-   [CSS tutorials](/css/tutorials)
-   [CSS properties reference](/css/properties)
