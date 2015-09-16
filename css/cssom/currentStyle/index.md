---
title: currentStyle
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/currentStyle_backgroundColor.htm'
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/currentStyle2.htm'
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/currentStyle_table.htm'
notes:
  - 'Non-standard; deletion candidate'
readiness: 'Not Ready'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: CSSStyleDeclaration
    href: /css/cssom/CSSStyleDeclaration/CSSStyleDeclaration
summary: 'Non standard. Gets the computed style declaration. Use getComputedStyle instead.'
tags:
  - API
  - Objects
  - DOM
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/methods/setAttribute
    - dom/methods/getAttribute
    - css/selectors/box-sizing
    - dom/properties/constructor
    - css/properties/ms-grid-column-align
    - css/properties/ms-grid-columns
    - css/properties/ms-grid-row
    - css/properties/ms-grid-row-align
    - css/properties/ms-grid-rows
    - css/properties/ms-grid-row-span
    - css/selectors/-ms-progress-appearance
    - css/selectors/-ms-scrollbar-3d-light-color
    - css/selectors/-ms-scrollbar-arrow-color
    - css/selectors/-ms-scrollbar-base-color
    - css/selectors/-ms-scrollbar-darkshadow-color
    - css/selectors/-ms-scrollbar-face-color
    - css/selectors/-ms-scrollbar-highlight-color
    - css/selectors/-ms-scrollbar-track-color
uri: css/cssom/currentStyle

---
## Summary

Non standard. Gets the computed style declaration. Use getComputedStyle instead.

Inherits from [CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)

## Properties

*No properties.*

## Methods

*No methods.*

## Events

*No events.*

## Inherited from CSSStyleDeclaration

### Properties

API Name
:   Summary

[cssText](/css/cssom/CSSStyleDeclaration/cssText)
:   Gets or sets the textual representation of a CSS style declaration.

[item](/css/cssom/CSSStyleDeclaration/item)
:

[background](/css/cssom/properties/background)
:   The background-position property sets the starting position of a background image.

[clipBottom](/css/cssom/properties/clipBottom)
:   Gets the bottom coordinate of the object clipping region.

[clipRight](/css/cssom/properties/clipRight)
:

[clipTop](/css/cssom/properties/clipTop)
:

[cssFloat](/css/cssom/properties/cssFloat)
:

[fontWeight](/css/cssom/properties/fontWeight)
:   Gets or sets the weight of the font of the object.

[hasLayout](/css/cssom/properties/hasLayout)
:

[height](/css/cssom/properties/height)
:   Sets the height of an element.

[width](/css/cssom/properties/width)
:   Sets the width of an element.

### Methods

API Name
:   Summary

[getPropertyPriority](/css/cssom/CSSStyleDeclaration/getPropertyPriority)
:   Gets the priority of a property in a CSS style declaration.

[getPropertyValue](/css/cssom/CSSStyleDeclaration/getPropertyValue)
:   Gets the value of a property in a CSS style declaration.

[removeProperty](/css/cssom/CSSStyleDeclaration/removeProperty)
:   Removes a property from a CSS style declaration.

[msGetPropertyEnabled](/css/cssom/methods/msGetPropertyEnabled)
:   Non standard. Indicates whether a property is enabled.

[msPutPropertyEnabled](/css/cssom/methods/msPutPropertyEnabled)
:   Non standard. Sets a property as enabled or disabled.

### Events

*No events.*

## Examples

This example uses the **currentStyle** object to set the text color to brown. If you click a colored area and the background color is the same as the text color, the checkColor function changes the background color, so the text can be read. Otherwise, the function takes no action.

This example works only if the body and text colors are set using either color names or red-green-blue hexadecimal values, but not a mix of the two.

``` html
<script>
function checkColor(element) {
  if (element.currentStyle.backgroundColor == 'brown') {
        element.style.backgroundColor = 'white';
    }
}
</script>
</head>
<p style="background-color: 'brown'"
    onclick="checkColor(this)">Click me</p>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/currentStyle_backgroundColor.htm)

This example uses the **currentStyle** object to retrieve values of the user-defined property created in the style rule. The alert returns the value `myvalue`.

``` html
<style>
    p { myproperty:myvalue }
</style>
<body>
<p id="oPrgrph" />
<script>
console.log(document.getElementById("oPrgrph").currentStyle.myproperty);
</script>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/currentStyle2.htm)

This example shows that the **td** object width returned by the **currentStyle** object is its cascaded width value rather than the width rendered on the screen.

``` html
<body id="oBdy">
<table border>
<tr><td width="1100" id="oTblD">text</td></tr>
</table>
<script>
console.log("The TD object currentStyle.width is " + document.getElementById("oTblD").currentStyle.width +
    ".\nThe width of the window is " + document.getElementById("oBdy").clientWidth +
    "px.\nThe width of the screen is " + screen.width + "px." );
</script>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/currentStyle_table.htm)

## Notes

The **currentStyle** object returns the cascaded styles on an element, but the [**style**](/css/cssom/style) object returns only the styles that have been applied inline on an element through the **style** attribute. Thus, the style values retrieved through the **currentStyle** object might differ from the style values retrieved through the **style** object. For example, if the [**color**](/css/properties/color) property is set on a paragraph only through a linked or embedded style sheet, and not inline, then object.**currentStyle**.color returns the color, whereas object.**style**.**color** does not return a value. If, however, the author specifies \<P STYLE="color:'red'", the **currentStyle** and **style** objects return the value . The **currentStyle** object reflects the order of style precedence in cascading style sheets (CSS). The CSS order of precedence for the presentation of HTML is:

1.  Inline styles
2.  Style sheet rules
3.  Attributes on HTML tags
4.  Intrinsic definition of the HTML tag

Accordingly, the **currentStyle** object returns the [**fontWeight**](/css/properties/font-weight) value **normal** on a bold tag if **normal** is specified in a style sheet. The **currentStyle** object returns values that reflect the applied style settings for the page and might not reflect what is rendering at the time a value is retrieved. For example, an object that has `"color:red; display:none"` returns **currentStyle**.color as even though the object is not rendered on the page. The **currentStyle** object, then, is not affected by the rendering constraints. The third example in the Example section demonstrates this behavior. Disabled style sheets also do not affect **currentStyle** values. The returned value is in the same units as those used to set the object. For example, if the color of an object is set inline using `STYLE="color:'green'"`, then **currentStyle**.color returns and not `#00FF00` (the red-green-blue hexadecimal equivalent to green). However, capitalization and redundant white space that appear in the object values set by the author are lost when the **currentStyle** object returns the object values. The **currentStyle** object supports user-defined properties in style rules. See the second example in the Example section. The **currentStyle** object is asynchronous. This means a style cannot be set and then immediately queried—instead, the old value is returned. Thus, for a script to obtain the expected behavior of **currentStyle** with methods such as [**addImport**](/css/cssom/styleSheet/addImport), the script needs to include a function that calls the method and a function that checks **currentStyle**. For a script to check the current style while a page is loading, the script must wait until the **body** element is loaded and the page has rendered, or the value of **currentStyle** might not reflect what is being displayed. This object is available in script as of Microsoft Internet Explorer 5. Windows Internet Explorer 8 or later. The behavior of the [**setAttribute**](/w/index.php?title=dom/methods/setAttribute&action=edit&redlink=1) method and the default value of the [**zIndex**](/css/properties/z-index) property varies according to the current document compatibility mode. For more information, see Attribute Differences in Internet Explorer 8 and Defining Document Compatibility.

### Members (MSDN)

The **currentStyle** object has these types of members:

-   [Additional Methods](#Additional_Methods)
-   [Additional Properties](#Additional_Properties)

#### Additional Methods

The **currentStyle** object has these methods.

|Method|Description|
|:-----|:----------|
|[**getAttribute**](/w/index.php?title=dom/methods/getAttribute&action=edit&redlink=1)|Retrieves the value of the specified attribute.|
|[**getExpression**](/css/cssom/methods/getExpression)|Retrieves the expression for the given property.|
|[**getPropertyPriority**](/css/cssom/CSSStyleDeclaration/getPropertyPriority)|Gets the priority of a CSS property if the priority is explicitly set in the current declaration block.|
|[**getPropertyValue**](/css/cssom/CSSStyleDeclaration/getPropertyValue)|Gets the value of a CSS property if it is explicitly set within the current declaration block.|
|[**item**](/css/cssom/CSSStyleDeclaration/item)|Gets a property that has been explicitly set in the current declaration block.|
|[**removeProperty**](/css/cssom/methods/removeProperty)|Removes a CSS property if it is explicitly set within the current declaration block.|
|[**setAttribute**](/w/index.php?title=dom/methods/setAttribute&action=edit&redlink=1)|Sets the value of the specified attribute.|
|[**setExpression**](/css/cssom/methods/setExpression)|Sets an expression for the specified object.|
|[**setProperty**](/css/cssom/methods/setProperty)|Sets a property value and priority within the current declaration block.|

#### Additional Properties

The **currentStyle** object has these properties.

<table>
<col width="50%" />
<col width="50%" />
<thead>
<tr class="header">
<th align="left">Property</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><a href="/css/media_queries/accelerator"><strong>accelerator</strong></a></td>
<td align="left">Sets or retrieves a string that indicates whether the object represents a keyboard shortcut.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/animation/animation"><strong>animation</strong></a></td>
<td align="left">Gets or sets one or more shorthand values that specify all animation properties (except <a href="/css/properties/animation-play-state"><strong>animation-play-state</strong></a>) for a set of corresponding object properties identified in the CSS <a href="/css/atrules/@keyframes"><strong>@keyframes</strong></a> at-rule specified by the <a href="/css/properties/animation-name"><strong>animation-name</strong></a> property.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/animation-delay"><strong>animationDelay</strong></a></td>
<td align="left">Gets or sets one or more values that specify the offset within an animation cycle (the amount of time from the start of a cycle) before the animation is displayed for a set of corresponding object properties identified in the CSS <a href="/css/atrules/@keyframes"><strong>@keyframes</strong></a> at-rule specified by the <a href="/css/properties/animation-name"><strong>animation-name</strong></a> property.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/animation-direction"><strong>animationDirection</strong></a></td>
<td align="left">Gets or sets one or more values that specify the direction of play for an animation cycle.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/animation-duration"><strong>animationDuration</strong></a></td>
<td align="left">Gets or sets one or more values that specify the length of time to complete one cycle of the animation.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/animation-fill-mode"><strong>animationFillMode</strong></a></td>
<td align="left">Gets or sets one or more values that specify whether the effects of an animation are visible before or after it plays.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/animation-iteration-count"><strong>animationIterationCount</strong></a></td>
<td align="left">Gets or sets one or more values that specify the number of times an animation cycle is played.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/animation-name"><strong>animationName</strong></a></td>
<td align="left">Gets or sets a value that identifies one or more animation names. An animation name identifies (or selects) a CSS <a href="/css/atrules/@keyframes"><strong>@keyframes</strong></a> at-rule.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/animation-play-state"><strong>animationPlayState</strong></a></td>
<td align="left">Gets or sets one or more values that specify whether an animation is playing or paused.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/animation-timing-function"><strong>animationTimingFunction</strong></a></td>
<td align="left">Gets or sets one or more values that specify the intermediate property values to be used during a single cycle of an animation on a set of corresponding object properties identified in the CSS <a href="/css/atrules/@keyframes"><strong>@keyframes</strong></a> at-rule specified by the <a href="/css/properties/animation-name"><strong>animationName</strong></a> property.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/backface-visibility"><strong>backfaceVisibility</strong></a></td>
<td align="left">Gets or sets a value that specifies whether the back face (reverse side) of an object is visible.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/cssom/properties/background"><strong>background</strong></a></td>
<td align="left">Sets or retrieves up to five separate background properties of the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/background-attachment"><strong>backgroundAttachment</strong></a></td>
<td align="left">Sets or retrieves how the background image is attached to the object within the document.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/background-clip"><strong>backgroundClip</strong></a></td>
<td align="left">Sets or retrieves the background painting area.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/background-color"><strong>backgroundColor</strong></a></td>
<td align="left">Sets or retrieves the color behind the content of the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/background-image"><strong>backgroundImage</strong></a></td>
<td align="left">Sets or retrieves the background image of the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/background-origin"><strong>backgroundOrigin</strong></a></td>
<td align="left">Sets or retrieves the background positioning area of a box or multiple boxes.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/background-position"><strong>backgroundPosition</strong></a></td>
<td align="left">Sets or retrieves the position of the background of the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/background-position-x"><strong>backgroundPositionX</strong></a></td>
<td align="left">Sets or retrieves the x-coordinate of the <a href="/css/properties/background-position"><strong>background-position</strong></a> property.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/background-position-y"><strong>backgroundPositionY</strong></a></td>
<td align="left">Sets or retrieves the y-coordinate of the <a href="/css/properties/background-position"><strong>background-position</strong></a> property.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/background-repeat"><strong>backgroundRepeat</strong></a></td>
<td align="left">Sets or retrieves how the <a href="/css/properties/background-image"><strong>background-image</strong></a> property of the object is tiled.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/background-size"><strong>backgroundSize</strong></a></td>
<td align="left">Sets or retrieves the size of the background images.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/svg/attributes/baseline-shift"><strong>baselineShift</strong></a></td>
<td align="left">Sets or retrieves a value that indicates how the dominant baseline should be repositioned relative to the dominant baseline of the parent text content element.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/media_queries/behavior"><strong>behavior</strong></a></td>
<td align="left">Sets or retrieves the location of the Dynamic HTML (DHTML) behavior.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/cssom/styleSheet/blockDirection"><strong>blockDirection</strong></a></td>
<td align="left">Gets a string value that indicates whether the content in the block element flows from left to right, or from right to left.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/border"><strong>border</strong></a></td>
<td align="left">Sets or retrieves the properties to draw around the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/border-bottom"><strong>borderBottom</strong></a></td>
<td align="left">Sets or retrieves the properties of the bottom border of the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/border-bottom-color"><strong>borderBottomColor</strong></a></td>
<td align="left">Sets or retrieves the color of the bottom border of the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/border-bottom-left-radius"><strong>borderBottomLeftRadius</strong></a></td>
<td align="left">Sets or retrieves one or two values that define the radii of the quarter ellipse that defines the shape of the lower-left corner for the outer border edge of the current box.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/border-bottom-right-radius"><strong>borderBottomRightRadius</strong></a></td>
<td align="left">Sets or retrieves one or two values that define the radii of the quarter ellipse that defines the shape of the lower-right corner for the outer border edge of the current box.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/border-bottom-style"><strong>borderBottomStyle</strong></a></td>
<td align="left">Sets or retrieves the style of the bottom border of the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/border-bottom-width"><strong>borderBottomWidth</strong></a></td>
<td align="left">Sets or retrieves the width of the bottom border of the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/border-collapse"><strong>borderCollapse</strong></a></td>
<td align="left">Sets or retrieves a value that indicates whether the row and cell borders of a table are joined in a single border or detached as in standard HTML.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/border-color"><strong>borderColor</strong></a></td>
<td align="left">Sets or retrieves the border color of the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/border-left"><strong>borderLeft</strong></a></td>
<td align="left">Sets or retrieves the properties of the left border of the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/border-left-color"><strong>borderLeftColor</strong></a></td>
<td align="left">Sets or retrieves the color of the left border of the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/border-left-style"><strong>borderLeftStyle</strong></a></td>
<td align="left">Sets or retrieves the style of the left border of the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/border-left-width"><strong>borderLeftWidth</strong></a></td>
<td align="left">Sets or retrieves the width of the left border of the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/border-radius"><strong>borderRadius</strong></a></td>
<td align="left">Sets or retrieves one or more values that define the radii of a quarter ellipse that defines the shape of the corners for the outer border edge of the current box.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/border-right"><strong>borderRight</strong></a></td>
<td align="left">Sets or retrieves the properties of the right border of the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/border-right-color"><strong>borderRightColor</strong></a></td>
<td align="left">Sets or retrieves the color of the right border of the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/border-right-style"><strong>borderRightStyle</strong></a></td>
<td align="left">Sets or retrieves the style of the right border of the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/border-right-width"><strong>borderRightWidth</strong></a></td>
<td align="left">Sets or retrieves the width of the right border of the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/border-spacing"><strong>borderSpacing</strong></a></td>
<td align="left">Sets or retrieves
<p>the distance between the borders of adjoining cells in a table.</p></td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/border-style"><strong>borderStyle</strong></a></td>
<td align="left">Sets or retrieves the style of the left, right, top, and bottom borders of the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/border-top"><strong>borderTop</strong></a></td>
<td align="left">Sets or retrieves the properties of the top border of the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/border-top-color"><strong>borderTopColor</strong></a></td>
<td align="left">Sets or retrieves the color of the top border of the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/border-top-left-radius"><strong>borderTopLeftRadius</strong></a></td>
<td align="left">Sets or retrieves one or two values that define the radii of the quarter ellipse that defines the shape of the upper-left corner for the outer border edge of the current box.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/border-top-right-radius"><strong>borderTopRightRadius</strong></a></td>
<td align="left">Sets or retrieves one or two values that define the radii of the quarter ellipse that defines the shape of the upper-right corner for the outer border edge of the current box.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/border-top-style"><strong>borderTopStyle</strong></a></td>
<td align="left">Sets or retrieves the style of the top border of the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/border-top-width"><strong>borderTopWidth</strong></a></td>
<td align="left">Sets or retrieves the width of the top border of the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/border-width"><strong>borderWidth</strong></a></td>
<td align="left">Sets or retrieves the width of the left, right, top, and bottom borders of the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/bottom"><strong>bottom</strong></a></td>
<td align="left">Sets or retrieves the bottom position of the object in relation to the bottom of the next positioned object in the document hierarchy.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/box-shadow"><strong>boxShadow</strong></a></td>
<td align="left">Sets or retrieves a comma-separated list of shadows that attaches one or more drop shadows to the current box.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/w/index.php?title=css/selectors/box-sizing&amp;action=edit&amp;redlink=1"><strong>boxSizing</strong></a></td>
<td align="left">Sets or retrieves
<p>the box model to use for object sizing.</p></td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/break-after"><strong>breakAfter</strong></a></td>
<td align="left">Gets or sets the column-break behavior that follows a content block in a multi-column element.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/break-before"><strong>breakBefore</strong></a></td>
<td align="left">Gets or sets the column-break behavior that precedes a content block in a multi-column element.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/break-inside"><strong>breakInside</strong></a></td>
<td align="left">Gets or sets the column-break behavior that occurs within a content block in a multi-column element.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/caption-side"><strong>captionSide</strong></a></td>
<td align="left">Sets or retrieves
<p>where the <strong>caption</strong> of a <a href="/html/elements/table"><strong>table</strong></a> is located.</p></td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/clear"><strong>clear</strong></a></td>
<td align="left">Sets or retrieves whether the object allows floating objects on its left side, right side, or both, so that the next text displays past the floating objects.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/clip"><strong>clip</strong></a></td>
<td align="left">Sets or retrieves which part of a positioned object is visible.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/cssom/properties/clipBottom"><strong>clipBottom</strong></a></td>
<td align="left">Gets the bottom coordinate of the object clipping region.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/cssom/properties/clipLeft"><strong>clipLeft</strong></a></td>
<td align="left">Gets the left coordinate of the object clipping region.</td>
</tr>
<tr class="even">
<td align="left"><a href="/svg/properties/clipPath"><strong>clipPath</strong></a></td>
<td align="left">Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/cssom/properties/clipRight"><strong>clipRight</strong></a></td>
<td align="left">Gets the right coordinate of the object clipping region.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/cssom/properties/clipTop"><strong>clipTop</strong></a></td>
<td align="left">Gets the top coordinate of the object clipping region.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/color"><strong>color</strong></a></td>
<td align="left">Sets or retrieves the color of the text of the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/column-count"><strong>columnCount</strong></a></td>
<td align="left">Gets or sets the optimal number of columns in a multi-column element.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/column-fill"><strong>columnFill</strong></a></td>
<td align="left">Gets or sets a value that indicates how the column lengths in a multi-column element are affected by the content flow.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/column-gap"><strong>columnGap</strong></a></td>
<td align="left">Gets or sets the width of the gap between columns in a multi-column element.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/column-rule"><strong>columnRule</strong></a></td>
<td align="left">Gets or sets a shorthand value that specifies values for the <a href="/css/properties/column-rule-width"><strong>columnRuleWidth</strong></a>, <a href="/css/properties/column-rule-style"><strong>columnRuleStyle</strong></a>, and the <a href="/css/properties/column-rule-color"><strong>columnRuleColor</strong></a> of a multi-column element.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/column-rule-color"><strong>columnRuleColor</strong></a></td>
<td align="left">Gets or sets the color for all column rules in a multi-column element.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/column-rule-style"><strong>columnRuleStyle</strong></a></td>
<td align="left">Gets or sets the style for all column rules in a multi-column element.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/column-rule-width"><strong>columnRuleWidth</strong></a></td>
<td align="left">Gets or sets the width of all column rules in a multi-column element.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/column-span"><strong>columnSpan</strong></a></td>
<td align="left">Gets or sets the number of columns that a content block spans in a multi-column element.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/column-width"><strong>columnWidth</strong></a></td>
<td align="left">Gets or sets the optimal width of the columns in a multi-column element.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/w/index.php?title=dom/properties/constructor&amp;action=edit&amp;redlink=1"><strong>constructor</strong></a></td>
<td align="left">Returns a reference to the constructor of an object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/content"><strong>content</strong></a></td>
<td align="left">Sets or retrieves
<p>generated content to insert before or after an element.</p></td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/counter-increment"><strong>counterIncrement</strong></a></td>
<td align="left">Sets or retrieves
<p>a list of counters to increment.</p></td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/counter-reset"><strong>counterReset</strong></a></td>
<td align="left">Sets or retrieves
<p>a list of counters to create or reset to zero.</p></td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/cssom/properties/cssFloat"><strong>cssFloat</strong></a></td>
<td align="left">Sets or retrieves a value that specifies whether a box should float to the left, right, or not at all.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/cssom/styleSheet/cssText"><strong>cssText</strong></a></td>
<td align="left">Sets or retrieves the persisted representation of the style rule.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/selectors/cursor"><strong>cursor</strong></a></td>
<td align="left">Sets or retrieves the type of cursor to display as the mouse pointer moves over the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/direction"><strong>direction</strong></a></td>
<td align="left">Sets or retrieves the reading order of the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/display"><strong>display</strong></a></td>
<td align="left">Gets or sets a value that indicates whether and how the object is rendered.</td>
</tr>
<tr class="even">
<td align="left"><a href="/svg/attributes/dominant-baseline"><strong>dominantBaseline</strong></a></td>
<td align="left">Sets or retrieves a value that determines or redetermines a scaled-baseline table.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/empty-cells"><strong>emptyCells</strong></a></td>
<td align="left">Determines whether to show or hide a cell without content.</td>
</tr>
<tr class="even">
<td align="left"><a href="/svg/attributes/fill"><strong>fill</strong></a></td>
<td align="left">Sets or retrieves a value that indicates the color to paint the interior of the given graphical element.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/svg/attributes/fill-opacity"><strong>fillOpacity</strong></a></td>
<td align="left">Sets or retrieves a value that specifies the opacity of the painting operation that is used to paint the interior of the current object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/svg/attributes/fill-rule"><strong>fillRule</strong></a></td>
<td align="left">Sets or retrieves a value that indicates the algorithm that is to be used to determine what parts of the canvas are included inside the shape.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/media_queries/filter"><strong>filter</strong></a></td>
<td align="left">Sets or retrieves the filter or collection of filters that are applied to the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/font"><strong>font</strong></a></td>
<td align="left">Sets or retrieves a combination of separate <a href="/css/properties/font"><strong>font</strong></a> properties of the object. Alternatively, sets or retrieves one or more of six user-preference fonts.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/font-family"><strong>fontFamily</strong></a></td>
<td align="left">Sets or retrieves the name of the font used for text in the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/font-size"><strong>fontSize</strong></a></td>
<td align="left">Sets or retrieves a value that indicates the font size used for text in the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/font-size-adjust"><strong>fontSizeAdjust</strong></a></td>
<td align="left">Sets or retrieves a value that specifies an aspect value for an element that will effectively preserve the x-height of the first choice font, whether it is substituted or not.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/font-stretch"><strong>fontStretch</strong></a></td>
<td align="left">Sets or retrieves a value that indicates a normal, condensed, or expanded face of a font family.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/font-style"><strong>fontStyle</strong></a></td>
<td align="left">Sets or retrieves the font style of the object as <strong>italic</strong>, <strong>normal</strong>, or <strong>oblique</strong>.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/fonts/font-variant"><strong>fontVariant</strong></a></td>
<td align="left">Gets or sets whether the text of the object is in small capital letters.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/cssom/properties/fontWeight"><strong>fontWeight</strong></a></td>
<td align="left">Gets the numeric weight of the font of the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/font-weight"><strong>fontWeight</strong></a></td>
<td align="left">Gets of sets the weight of the font of the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/svg/attributes/glyph-orientation-horizontal"><strong>glyphOrientationHorizontal</strong></a></td>
<td align="left">Sets or retrieves a value that alters the orientation of a sequence of characters relative to an inline-progression-direction of horizontal.</td>
</tr>
<tr class="even">
<td align="left"><a href="/svg/attributes/glyph-orientation-vertical"><strong>glyphOrientationVertical</strong></a></td>
<td align="left">Sets or retrieves a value that alters the orientation of a sequence of characters relative to an inline-progression-direction of vertical.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/cssom/properties/hasLayout"><strong>hasLayout</strong></a></td>
<td align="left">Gets a value that indicates whether the object has layout.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/height"><strong>height</strong></a></td>
<td align="left">Sets or retrieves the height of the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/ime-mode"><strong>imeMode</strong></a></td>
<td align="left">Sets or retrieves the state of an IME.</td>
</tr>
<tr class="even">
<td align="left"><a href="/svg/attributes/kerning"><strong>kerning</strong></a></td>
<td align="left">Gets or sets a value that indicates whether Internet Explorer should adjust inter-glyph spacing based on kerning tables that are included in the relevant font (that is, enable auto-kerning) or instead disable auto-kerning and set inter-character spacing to a specific length (typically zero).
<p>Gets or sets a value that indicates whether the user-agent should adjust inter-glyph spacing based on kerning tables that are included in the relevant font (that is, enable auto-kerning) or instead disable auto-kerning and set inter-character spacing to a specific length (typically zero).</p></td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/layout-flow"><strong>layoutFlow</strong></a></td>
<td align="left">Sets or retrieves the direction and flow of the content in the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/layout-grid"><strong>layoutGrid</strong></a></td>
<td align="left">Sets or retrieves the composite document grid properties that specify the layout of text characters.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/layout-grid-char"><strong>layoutGridChar</strong></a></td>
<td align="left">Sets or retrieves the size of the character grid used for rendering the text content of an element.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/layout-grid-line"><strong>layoutGridLine</strong></a></td>
<td align="left">Sets or retrieves the gridline value used for rendering the text content of an element.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/layout-grid-mode"><strong>layoutGridMode</strong></a></td>
<td align="left">Gets or sets whether the text layout grid uses two dimensions.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/layout-grid-type"><strong>layoutGridType</strong></a></td>
<td align="left">Sets or retrieves the type of grid used for rendering the text content of an element.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/left"><strong>left</strong></a></td>
<td align="left">Sets or retrieves the position of the object relative to the left edge of the next positioned object in the document hierarchy.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/cssom/properties/length"><strong>length</strong></a></td>
<td align="left">Retrieves the number of properties that are explicitly set on the parent object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/letter-spacing"><strong>letterSpacing</strong></a></td>
<td align="left">Sets or retrieves the amount of additional space between letters in the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/line-break"><strong>lineBreak</strong></a></td>
<td align="left">Deprecated. Gets or sets
<p>line-breaking rules for text in selected languages such as Japanese, Chinese, and Korean.</p></td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/line-height"><strong>lineHeight</strong></a></td>
<td align="left">Sets or retrieves the distance between lines in the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/list-style"><strong>listStyle</strong></a></td>
<td align="left">Sets or retrieves up to three separate <a href="/css/properties/list-style"><strong>list-style</strong></a> properties of the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/list-style-image"><strong>listStyleImage</strong></a></td>
<td align="left">Sets or retrieves a value that indicates which image to use as a list-item marker for the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/list-style-position"><strong>listStylePosition</strong></a></td>
<td align="left">Sets or retrieves a variable that indicates how the list-item marker is drawn relative to the content of the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/list-style-type"><strong>listStyleType</strong></a></td>
<td align="left">Sets or retrieves the predefined type of the line-item marker for the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/margin"><strong>margin</strong></a></td>
<td align="left">Sets or retrieves the width of the top, right, bottom, and left margins of the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/margin-bottom"><strong>marginBottom</strong></a></td>
<td align="left">Sets or retrieves the height of the bottom margin of the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/margin-left"><strong>marginLeft</strong></a></td>
<td align="left">Sets or retrieves the width of the left margin of the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/margin-right"><strong>marginRight</strong></a></td>
<td align="left">Sets or retrieves the width of the right margin of the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/margin-top"><strong>marginTop</strong></a></td>
<td align="left">Sets or retrieves the height of the top margin of the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/svg/attributes/marker"><strong>marker</strong></a></td>
<td align="left">Sets or retrieves a value that specifies the marker symbol that is used for all vertices on the given <a href="/svg/elements/path"><strong>path</strong></a> element or basic shape.</td>
</tr>
<tr class="even">
<td align="left"><a href="/svg/attributes/marker-end"><strong>markerEnd</strong></a></td>
<td align="left">Sets or retrieves a value that defines the arrowhead or polymarker that is drawn at the final vertex of a given <a href="/svg/elements/path"><strong>path</strong></a> element or basic shape.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/svg/attributes/marker-mid"><strong>markerMid</strong></a></td>
<td align="left">Sets or retrieves a value that defines the arrowhead or polymarker that is drawn at every other vertex (that is, every vertex except the first and last) of a given <a href="/svg/elements/path"><strong>path</strong></a> element or basic shape.</td>
</tr>
<tr class="even">
<td align="left"><a href="/svg/attributes/marker-start"><strong>markerStart</strong></a></td>
<td align="left">Sets or retrieves a value that defines the arrowhead or polymarker that is drawn at the first vertex of a given <a href="/svg/elements/path"><strong>path</strong></a> element or basic shape.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/svg/attributes/mask"><strong>mask</strong></a></td>
<td align="left">Sets or retrieves a value that indicates a SVG mask.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/max-height"><strong>maxHeight</strong></a></td>
<td align="left">Sets or retrieves the maximum height for an element.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/max-width"><strong>maxWidth</strong></a></td>
<td align="left">Sets or retrieves the maximum width for an element.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/min-height"><strong>minHeight</strong></a></td>
<td align="left">Sets or retrieves the minimum height for an element.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/min-width"><strong>minWidth</strong></a></td>
<td align="left">Sets or retrieves the minimum width for an element.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/ms-block-progression"><strong>msBlockProgression</strong></a></td>
<td align="left">Sets or retrieves the block progression and layout orientation.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/ms-box-align"><strong>msBoxAlign</strong></a></td>
<td align="left">Do not use. This property has been replaced by the <a href="/css/properties/ms-flex-align"><strong>-ms-flex-align</strong></a> property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/ms-box-direction"><strong>msBoxDirection</strong></a></td>
<td align="left">Do not use. This property has been replaced by the <a href="/css/properties/ms-flex-direction"><strong>-ms-flex-direction</strong></a> property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/ms-box-flex"><strong>msBoxFlex</strong></a></td>
<td align="left">Do not use. This property has been replaced by the <a href="/css/properties/ms-flex"><strong>-ms-flex</strong></a> property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/ms-box-line-progression"><strong>msBoxLineProgression</strong></a></td>
<td align="left">Do not use. This property has been replaced by the <a href="/css/properties/ms-flex-wrap"><strong>-ms-flex-wrap</strong></a> property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/ms-box-lines"><strong>msBoxLines</strong></a></td>
<td align="left">Do not use. This property has been replaced by the <a href="/css/properties/ms-flex-wrap"><strong>-ms-flex-wrap</strong></a> property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/ms-box-ordinal-group"><strong>msBoxOrdinalGroup</strong></a></td>
<td align="left">Do not use. This property has been replaced by the <a href="/css/properties/ms-flex-order"><strong>-ms-flex-order</strong></a> property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/ms-box-orient"><strong>msBoxOrient</strong></a></td>
<td align="left">Do not use. This property has been replaced by the <a href="/css/properties/ms-flex-direction"><strong>-ms-flex-direction</strong></a> property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/ms-grid-column"><strong>msGridColumn</strong></a></td>
<td align="left">Gets or sets a value that specifies in which column of the grid to place the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/w/index.php?title=css/properties/ms-grid-column-align&amp;action=edit&amp;redlink=1"><strong>msGridColumnAlign</strong></a></td>
<td align="left">Gets or sets a value that specifies the horizontal alignment of the object within the grid column.</td>
</tr>
<tr class="even">
<td align="left"><a href="/w/index.php?title=css/properties/ms-grid-columns&amp;action=edit&amp;redlink=1"><strong>msGridColumns</strong></a></td>
<td align="left">Gets or sets one or more values that specify the width of each grid column within the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/ms-grid-column-span"><strong>msGridColumnSpan</strong></a></td>
<td align="left">Gets or sets a value that specifies the number of columns of the grid that the object spans.</td>
</tr>
<tr class="even">
<td align="left"><a href="/w/index.php?title=css/properties/ms-grid-row&amp;action=edit&amp;redlink=1"><strong>msGridRow</strong></a></td>
<td align="left">Gets or sets a value that specifies in which row of the grid to place the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/w/index.php?title=css/properties/ms-grid-row-align&amp;action=edit&amp;redlink=1"><strong>msGridRowAlign</strong></a></td>
<td align="left">Gets or sets a value that specifies the vertical alignment of the object within the grid row.</td>
</tr>
<tr class="even">
<td align="left"><a href="/w/index.php?title=css/properties/ms-grid-rows&amp;action=edit&amp;redlink=1"><strong>msGridRows</strong></a></td>
<td align="left">Gets or sets one or more values that specify the height of each grid row within the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/w/index.php?title=css/properties/ms-grid-row-span&amp;action=edit&amp;redlink=1"><strong>msGridRowSpan</strong></a></td>
<td align="left">Gets or sets a value that specifies the number of rows of the grid that the object spans.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/media_queries/ms-interpolation-mode"><strong>msInterpolationMode</strong></a></td>
<td align="left">Obsolete. Gets or sets the interpolation (resampling) method used to stretch images.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/w/index.php?title=css/selectors/-ms-progress-appearance&amp;action=edit&amp;redlink=1"><strong>msProgressAppearance</strong></a></td>
<td align="left">This property is obsolete. Use <a href="/css/properties/animation-name"><strong>animation-name</strong></a> instead.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/opacity"><strong>opacity</strong></a></td>
<td align="left">Gets or sets a value that specifies object or group opacity in CSS or SVG.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/orphans"><strong>orphans</strong></a></td>
<td align="left">Sets or retrieves
<p>the minimum number of lines of a paragraph that must appear at the bottom of a page.</p></td>
</tr>
<tr class="even">
<td align="left"><a href="/css/selectors/outline"><strong>outline</strong></a></td>
<td align="left">Sets or retrieves
<p>the color, style, and width of the outline frame.</p></td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/selectors/outline-color"><strong>outlineColor</strong></a></td>
<td align="left">Sets or retrieves
<p>the color of the outline frame.</p></td>
</tr>
<tr class="even">
<td align="left"><a href="/css/selectors/outline-style"><strong>outlineStyle</strong></a></td>
<td align="left">Sets or retrieves
<p>the style of the outline frame.</p></td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/selectors/outline-width"><strong>outlineWidth</strong></a></td>
<td align="left">Sets or retrieves
<p>the width of the outline frame.</p></td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/overflow"><strong>overflow</strong></a></td>
<td align="left">Sets or retrieves a value indicating how to manage the content of the object when the content exceeds the height or width of the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/overflow-x"><strong>overflowX</strong></a></td>
<td align="left">Sets or retrieves how to manage the content of the object when the content exceeds the width of the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/overflow-y"><strong>overflowY</strong></a></td>
<td align="left">Sets or retrieves how to manage the content of the object when the content exceeds the height of the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/padding"><strong>padding</strong></a></td>
<td align="left">Sets or retrieves the amount of space to insert between the object and its margin or, if there is a border, between the object and its border.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/padding-bottom"><strong>paddingBottom</strong></a></td>
<td align="left">Sets or retrieves the amount of space to insert between the bottom border of the object and the content.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/padding-left"><strong>paddingLeft</strong></a></td>
<td align="left">Sets or retrieves the amount of space to insert between the left border of the object and the content.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/padding-right"><strong>paddingRight</strong></a></td>
<td align="left">Sets or retrieves the amount of space to insert between the right border of the object and the content.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/padding-top"><strong>paddingTop</strong></a></td>
<td align="left">Sets or retrieves the amount of space to insert between the top border of the object and the content.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/page-break-after"><strong>pageBreakAfter</strong></a></td>
<td align="left">Sets or retrieves a value indicating whether a page break occurs after the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/page-break-before"><strong>pageBreakBefore</strong></a></td>
<td align="left">Sets or retrieves a string indicating whether a page break occurs before the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/page-break-inside"><strong>pageBreakInside</strong></a></td>
<td align="left">Sets or retrieves
<p>a string indicating whether a page break is allowed to occur inside the object.</p></td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/cssom/CSSRule/parentRule"><strong>parentRule</strong></a></td>
<td align="left">Retrieves the containing rule, if the current rule is contained inside another rule.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/perspective"><strong>perspective</strong></a></td>
<td align="left">Gets or sets a value that represents the perspective from which all child elements of the object are viewed.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/perspective-origin"><strong>perspectiveOrigin</strong></a></td>
<td align="left">Gets or sets one or two values that represent the origin (the vanishing point for the 3-D space) of an object with an <a href="/css/properties/perspective"><strong>perspective</strong></a> property declaration.</td>
</tr>
<tr class="even">
<td align="left"><a href="/svg/attributes/pointers"><strong>pointerEvents</strong></a></td>
<td align="left">Sets or retrieves a value that specifies under what circumstances a given graphics element can be the target element for a pointer event in SVG.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/position"><strong>position</strong></a></td>
<td align="left">Sets or retrieves the type of positioning used for the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/quotes"><strong>quotes</strong></a></td>
<td align="left">Sets or retrieves the pairs of strings to be used as quotes in generated content.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/right"><strong>right</strong></a></td>
<td align="left">Sets or retrieves the position of the object relative to the right edge of the next positioned object in the document hierarchy.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/ruby-align"><strong>rubyAlign</strong></a></td>
<td align="left">Gets or sets a value that indicates how to align the ruby text content.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/ruby-overhang"><strong>rubyOverhang</strong></a></td>
<td align="left">Gets or sets a value that indicates whether, and on which side, ruby text is allowed to partially overhang any adjacent text in addition to its own base, when the ruby text is wider than the ruby base</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/ruby-position"><strong>rubyPosition</strong></a></td>
<td align="left">Gets or sets a value that controls the position of the ruby text with respect to its base.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/w/index.php?title=css/selectors/-ms-scrollbar-3d-light-color&amp;action=edit&amp;redlink=1"><strong>scrollbar3dLightColor</strong></a></td>
<td align="left">Sets or retrieves the color of the top and left edges of the scroll box and scroll arrows of a scroll bar.</td>
</tr>
<tr class="even">
<td align="left"><a href="/w/index.php?title=css/selectors/-ms-scrollbar-arrow-color&amp;action=edit&amp;redlink=1"><strong>scrollbarArrowColor</strong></a></td>
<td align="left">Sets or retrieves the color of the arrow elements of a scroll arrow.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/w/index.php?title=css/selectors/-ms-scrollbar-base-color&amp;action=edit&amp;redlink=1"><strong>scrollbarBaseColor</strong></a></td>
<td align="left">Sets or retrieves the color of the main elements of a scroll bar, which include the scroll box, track, and scroll arrows.</td>
</tr>
<tr class="even">
<td align="left"><a href="/w/index.php?title=css/selectors/-ms-scrollbar-darkshadow-color&amp;action=edit&amp;redlink=1"><strong>scrollbarDarkShadowColor</strong></a></td>
<td align="left">Sets or retrieves the color of the gutter of a scroll bar.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/w/index.php?title=css/selectors/-ms-scrollbar-face-color&amp;action=edit&amp;redlink=1"><strong>scrollbarFaceColor</strong></a></td>
<td align="left">Sets or retrieves the color of the scroll box and scroll arrows of a scroll bar.</td>
</tr>
<tr class="even">
<td align="left"><a href="/w/index.php?title=css/selectors/-ms-scrollbar-highlight-color&amp;action=edit&amp;redlink=1"><strong>scrollbarHighlightColor</strong></a></td>
<td align="left">Sets or retrieves the color of the top and left edges of the scroll box and scroll arrows of a scroll bar.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/selectors/-ms-scrollbar-shadow-color"><strong>scrollbarShadowColor</strong></a></td>
<td align="left">Sets or retrieves the color of the bottom and right edges of the scroll box and scroll arrows of a scroll bar.</td>
</tr>
<tr class="even">
<td align="left"><a href="/w/index.php?title=css/selectors/-ms-scrollbar-track-color&amp;action=edit&amp;redlink=1"><strong>scrollbarTrackColor</strong></a></td>
<td align="left">Sets or retrieves the color of the track element of a scroll bar.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/svg/attributes/stop-color"><strong>stopColor</strong></a></td>
<td align="left">Sets or retrieves a value that indicates what color to use at the current gradient stop.</td>
</tr>
<tr class="even">
<td align="left"><a href="/svg/attributes/stop-opacity"><strong>stopOpacity</strong></a></td>
<td align="left">Sets or retrieves a value that defines the opacity of the current gradient stop.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/svg/attributes/stroke"><strong>stroke</strong></a></td>
<td align="left">Sets or retrieves a value that indicates the color to paint along the outline of a given graphical element.</td>
</tr>
<tr class="even">
<td align="left"><a href="/svg/attributes/stroke-dasharray"><strong>strokeDasharray</strong></a></td>
<td align="left">Sets or retrieves one or more values that indicate the pattern of dashes and gaps used to stroke paths.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/svg/attributes/stroke-dashoffset"><strong>strokeDashoffset</strong></a></td>
<td align="left">Sets or retrieves a value that specifies the distance into the dash pattern to start the dash.</td>
</tr>
<tr class="even">
<td align="left"><a href="/svg/attributes/stroke-linecap"><strong>strokeLinecap</strong></a></td>
<td align="left">Sets or retrieves a value that specifies the shape to be used at the end of open subpaths when they are stroked.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/svg/attributes/stroke-linejoin"><strong>strokeLinejoin</strong></a></td>
<td align="left">Sets or retrieves a value that specifies the shape to be used at the corners of paths or basic shapes when they are stroked.</td>
</tr>
<tr class="even">
<td align="left"><a href="/svg/attributes/stroke-miterlimit"><strong>strokeMiterlimit</strong></a></td>
<td align="left">Sets or retrieves a value that indicates the limit on the ratio of the length of miter joins (as specified in the <a href="/svg/attributes/stroke-linejoin"><strong>strokeLinejoin</strong></a> property).</td>
</tr>
<tr class="odd">
<td align="left"><a href="/svg/attributes/stroke-opacity"><strong>strokeOpacity</strong></a></td>
<td align="left">Sets or retrieves a value that specifies the opacity of the painting operation that is used to stroke the current object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/svg/attributes/stroke-width"><strong>strokeWidth</strong></a></td>
<td align="left">Sets or retrieves a value that specifies the width of the stroke on the current object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/float"><strong>styleFloat</strong></a></td>
<td align="left">Sets or retrieves on which side of the object the text will flow.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/table-layout"><strong>tableLayout</strong></a></td>
<td align="left">Sets or retrieves a string that indicates whether the table layout is fixed.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/text-align"><strong>textAlign</strong></a></td>
<td align="left">Sets or retrieves whether the text in the object is left-aligned, right-aligned, centered, or justified.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/text-align-last"><strong>textAlignLast</strong></a></td>
<td align="left">Gets or sets a value that indicates how to align the last line or only line of text in the specified object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/text-autospace"><strong>textAutospace</strong></a></td>
<td align="left">Sets or retrieves the autospacing and narrow space width adjustment of text.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/text-decoration"><strong>textDecoration</strong></a></td>
<td align="left">Sets or retrieves a value that indicates whether the text in the object has blink, line-through, overline, or underline decorations.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/text-indent"><strong>textIndent</strong></a></td>
<td align="left">Sets or retrieves the indentation of the first line of text in the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/text-justify"><strong>textJustify</strong></a></td>
<td align="left">Sets or retrieves the type of alignment used to justify text in the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/text-kashida-space"><strong>textKashidaSpace</strong></a></td>
<td align="left">Sets or retrieves the ratio of kashida expansion to white space expansion when justifying lines of text in the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/text-overflow"><strong>textOverflow</strong></a></td>
<td align="left">Sets or retrieves a value that indicates whether to render ellipses (...) to indicate text overflow.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/text-transform"><strong>textTransform</strong></a></td>
<td align="left">Sets or retrieves the rendering of the text in the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/text-underline-position"><strong>textUnderlinePosition</strong></a></td>
<td align="left">Sets or retrieves the position of the underline decoration that is set through the <a href="/css/properties/text-decoration"><strong>text-decoration</strong></a> property of the object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/top"><strong>top</strong></a></td>
<td align="left">Sets or retrieves the position of the object relative to the top of the next positioned object in the document hierarchy.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/transforms/transform"><strong>transform</strong></a></td>
<td align="left">Gets or sets a list of one or more transform functions that specify how to translate, rotate, or scale an element in 2-D or 3-D space.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/transform-origin"><strong>transformOrigin</strong></a></td>
<td align="left">Gets or sets one or two values that establish the origin of transformation for an element.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/transform-style"><strong>transformStyle</strong></a></td>
<td align="left">Gets or sets a value that specifies how child elements of the object are rendered in 3-D space.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/transition"><strong>transition</strong></a></td>
<td align="left">Gets or sets one or more shorthand values that specify the transition properties for a set of corresponding object properties identified in the <a href="/css/properties/transition-property"><strong>transition-property</strong></a> property.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/transition-delay"><strong>transitionDelay</strong></a></td>
<td align="left">Gets or sets one or more values that specify the offset within a transition (the amount of time from the start of a transition) before the transition is displayed for a set of corresponding object properties identified in the <a href="/css/properties/transition-property"><strong>transition-property</strong></a> property.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/transition-duration"><strong>transitionDuration</strong></a></td>
<td align="left">Gets or sets one or more values that specify the durations of transitions on a set of corresponding object properties identified in the <a href="/css/properties/transition-property"><strong>transition-property</strong></a> property.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/transition-property"><strong>transitionProperty</strong></a></td>
<td align="left">Gets or sets a value that identifies the CSS property name or names to which the transition effect (defined by <a href="/css/properties/transition-duration"><strong>transition-duration</strong></a>, <a href="/css/functions/transition-timing-function"><strong>transition-timing-function</strong></a>, and <a href="/css/properties/transition-delay"><strong>transition-delay</strong></a>) is applied when a new property value is specified.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/functions/transition-timing-function"><strong>transitionTimingFunction</strong></a></td>
<td align="left">Gets or sets one or more values that specify the intermediate property values to be used during a transition on a set of corresponding object properties identified in the <a href="/css/properties/transition-property"><strong>transition-property</strong></a> property.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/unicode-bidi"><strong>unicodeBidi</strong></a></td>
<td align="left">Sets or retrieves the level of embedding with respect to the bidirectional algorithm.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/vertical-align"><strong>verticalAlign</strong></a></td>
<td align="left">Sets or retrieves the vertical alignment of the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/visibility"><strong>visibility</strong></a></td>
<td align="left">Sets or retrieves whether the content of the object is displayed.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/white-space"><strong>whiteSpace</strong></a></td>
<td align="left">Sets or retrieves a value that indicates whether lines are automatically broken inside the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/widows"><strong>widows</strong></a></td>
<td align="left">Sets or retrieves
<p>the minimum number of lines of a paragraph that must appear at the top of a document.</p></td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/width"><strong>width</strong></a></td>
<td align="left">Sets or retrieves the width of the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/word-break"><strong>wordBreak</strong></a></td>
<td align="left">Sets or retrieves
<p>line-breaking behavior within words, particularly where multiple languages appear in the object.</p></td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/text/word-spacing/word-spacing"><strong>wordSpacing</strong></a></td>
<td align="left">Sets or retrieves the amount of additional space between words in the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/word-wrap"><strong>wordWrap</strong></a></td>
<td align="left">Sets or retrieves whether to break words when the content exceeds the boundaries of its container.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/properties/writing-mode"><strong>writingMode</strong></a></td>
<td align="left">Sets or retrieves the direction and flow of the content in the object.</td>
</tr>
<tr class="even">
<td align="left"><a href="/css/properties/z-index"><strong>zIndex</strong></a></td>
<td align="left">Sets or retrieves the stacking order of positioned objects.</td>
</tr>
<tr class="odd">
<td align="left"><a href="/css/selectors/zoom"><strong>zoom</strong></a></td>
<td align="left">Sets or retrieves the magnification scale of the object.</td>
</tr>
</tbody>
</table>

## See also

### Related pages

-   `style`
