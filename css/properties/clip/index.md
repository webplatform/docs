---
title: clip
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/6338197'
notes:
  - "Add specifications, compatibility.\nDeprecated; replaced by clip-path."
overview_table:
  '[Initial value](/css/concepts/initial_value)': ''
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
summary: "Deprecated; see clip-path.\n"
tags:
  - CSS
  - Properties
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected
uri: css/properties/clip

---
## <span>Summary</span>

Deprecated; see clip-path.

Lets you specify the dimensions of an absolutely positioned element that should be visible, and the element is clipped into this shape, and displayed.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

## <span>Syntax</span>

-   `clip: auto`
-   `clip: rect(top, right, bottom, left)`

## <span>Values</span>

auto
:   Default. Clip to expose entire object.

rect(top, right, bottom, left)
:   Top, right, bottom, and left specify length values, any of which can be replaced by **auto**, leaving that side not clipped. The value of top specifies that everything above this value on the Y axis (with 0 at the top) is clipped. The value of right specifies that everything above this value on the X axis (with 0 at the left) is clipped. The value of bottom specifies that everything below this value on the Y axis (with 0 at the top) is clipped. The value of left specifies that everything to the left of this value on the X axis (with 0 at the left) is clipped.

## <span>Examples</span>

This example takes the Web Platform Docs logo and clips it in two ways: one shows the icon and the other shows the text.

``` css
img.clippable {
  /**
   * The `clip` property applies only to absolutely positioned elements only.
   * @see http://www.w3.org/TR/css-masking/#clip-property
   */
  position: absolute;
  top: 100px;
}

img.clipped-icon {
  left: 215px;
  /**
   * The rectangle clips the image leaving only the icon visible.
   * For Internet Explorer 4-7, use `clip: rect(10px 68px 63px 3px);`
   */
  clip: rect(10px, 68px, 63px, 3px);
}

img.clipped-text {
  left: 300px;
  /**
   * The rectangle clips the image leaving only the text visible.
   * For Internet Explorer 4-7, use `clip: rect(10px 190px 63px 53px);`
   */
  clip: rect(10px, 190px, 63px, 53px);
}
```

[View live example](http://code.webplatform.org/gist/6338197)

The HTML for the above example.

``` html


  <img class="clippable original" src="http://www.webplatform.org/logo/wplogo_pillow_wide_tan.png" alt="Web Platform Docs logo" />
  <img class="clippable clipped-icon" src="http://www.webplatform.org/logo/wplogo_pillow_wide_tan.png" alt="Web Platform Docs logo (icon only)" title="Web Platform Docs logo (icon only)" />
  <img class="clippable clipped-text" src="http://www.webplatform.org/logo/wplogo_pillow_wide_tan.png" alt="Web Platform Docs logo (text only)" title="Web Platform Docs logo (text only)" />
```

</pre>

## <span>Notes</span>

### <span>Remarks</span>

As of Windows Internet Explorer 8, the required syntax of the **clip** attribute is identical to that specified in the Cascading Style Sheets, Level 2 Revision 1 (CSS2.1) specification; that is, commas are now required between the parameters of the `rect()` value. This behavior requires Windows Internet Explorer to be in IE8 Standards mode (or EmulateIE8 mode with an Internet Explorer 8 [!DOCTYPE](/html/elements/!DOCTYPE) directive). For more information on document compatibility modes, see Defining Document Compatibility. In Windows Internet Explorer 7 and earlier (and in Internet Explorer 8 or later in IE7 Standards mode, EmulateIE7 mode, or IE5 (Quirks) mode), the commas should be omitted. For example: **clip**:`rect(0 50 50 0)` The required syntax of the **clip** attribute is identical to that specified in the CSS2.1 specification; that is, commas are now required between the parameters of the `rect()` value. This property defines the shape and size of the positioned object that is visible. The [**position**](/css/properties/position) must be set to **absolute**. Any part of the object that is outside the clipping region is transparent. Any coordinate can be replaced by the value **auto**, which exposes the respective side (that is, the side is not clipped). The order of the values **clip**:`rect(0, 0, 50, 50)` renders the object invisible because it sets the top and right positions of the clipping region to 0. To achieve a 50-by-50 view port, use **clip**:`rect(0, 50, 50, 0)`. The **clip** attribute and the **clip** property are available on the Macintosh platform, as of Microsoft Internet Explorer 5.

### <span>Syntax</span>

`clip: auto | rect(top, right, bottom, left)`

## <span>See also</span>

### <span>Related articles</span>

#### <span>Visual Effects</span>

-   [color](/css/color)

-   [Colors by Hue](/css/color/colors_by_hue)

-   [Colors by Name](/css/color/colors_by_name)

-   [Colors by Saturation](/css/color/colors_by_saturation)

-   [User-Defined System Colors](/css/color/user-defined_system_colors)

-   [-ms-high-contrast](/css/high_contrast_mode/properties/-ms-high-contrast)

-   [ms-high-contrast-adjust](/css/high_contrast_modeapis/properties/ms-high-contrast-adjust)

-   [-ms-progress-appearance](/css/properties/-ms-progress-appearance)

-   [background-blend-mode](/css/properties/background-blend-mode)

-   **clip**

-   [cursor](/css/properties/cursor)

-   [opacity](/css/properties/opacity)

-   [zoom](/css/properties/zoom)

-   [height](/html/attributes/height)

-   [blink](/html/elements/blink)

-   [filter](/svg/elements/filter)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

### <span>Related pages (MSDN)</span>

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `defaults`
-   `runtimeStyle`
-   `style`
-   `Reference`
-   `clipBottom`
-   `clipLeft`
-   `clipRight`
-   `clipTop`
