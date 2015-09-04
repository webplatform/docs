---
title: currentStyle
tags:
  - API
  - Objects
  - DOM
readiness: 'Not Ready'
notes:
  - 'Non-standard; deletion candidate'
summary: 'Non standard. Gets the computed style declaration. Use getComputedStyle instead.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/currentStyle_backgroundColor.htm'
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/currentStyle2.htm'
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/currentStyle_table.htm'
uri: css/cssom/currentStyle
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

---
# currentStyle

## Summary

Non standard. Gets the computed style declaration. Use getComputedStyle instead.

<span data-meta="subclass_of" data-type="key">Inherits from <span data-type="value">[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)</span></span>

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

``` {.html}
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

``` {.html}
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

``` {.html}
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

Method
:   Description
[**getAttribute**](/w/index.php?title=dom/methods/getAttribute&action=edit&redlink=1)
:   Retrieves the value of the specified attribute.
[**getExpression**](/css/cssom/methods/getExpression)
:   Retrieves the expression for the given property.
[**getPropertyPriority**](/css/cssom/CSSStyleDeclaration/getPropertyPriority)
:   Gets the priority of a CSS property if the priority is explicitly set in the current declaration block.
[**getPropertyValue**](/css/cssom/CSSStyleDeclaration/getPropertyValue)
:   Gets the value of a CSS property if it is explicitly set within the current declaration block.
[**item**](/css/cssom/CSSStyleDeclaration/item)
:   Gets a property that has been explicitly set in the current declaration block.
[**removeProperty**](/css/cssom/methods/removeProperty)
:   Removes a CSS property if it is explicitly set within the current declaration block.
[**setAttribute**](/w/index.php?title=dom/methods/setAttribute&action=edit&redlink=1)
:   Sets the value of the specified attribute.
[**setExpression**](/css/cssom/methods/setExpression)
:   Sets an expression for the specified object.
[**setProperty**](/css/cssom/methods/setProperty)
:   Sets a property value and priority within the current declaration block.

#### Additional Properties

The **currentStyle** object has these properties.

Property
:   Description
[**accelerator**](/css/media_queries/accelerator)
:   Sets or retrieves a string that indicates whether the object represents a keyboard shortcut.
[**animation**](/css/properties/animation/animation)
:   Gets or sets one or more shorthand values that specify all animation properties (except [**animation-play-state**](/css/properties/animation-play-state)) for a set of corresponding object properties identified in the CSS [**@keyframes**](/css/atrules/@keyframes) at-rule specified by the [**animation-name**](/css/properties/animation-name) property.
[**animationDelay**](/css/properties/animation-delay)
:   Gets or sets one or more values that specify the offset within an animation cycle (the amount of time from the start of a cycle) before the animation is displayed for a set of corresponding object properties identified in the CSS [**@keyframes**](/css/atrules/@keyframes) at-rule specified by the [**animation-name**](/css/properties/animation-name) property.
[**animationDirection**](/css/properties/animation-direction)
:   Gets or sets one or more values that specify the direction of play for an animation cycle.
[**animationDuration**](/css/properties/animation-duration)
:   Gets or sets one or more values that specify the length of time to complete one cycle of the animation.
[**animationFillMode**](/css/properties/animation-fill-mode)
:   Gets or sets one or more values that specify whether the effects of an animation are visible before or after it plays.
[**animationIterationCount**](/css/properties/animation-iteration-count)
:   Gets or sets one or more values that specify the number of times an animation cycle is played.
[**animationName**](/css/properties/animation-name)
:   Gets or sets a value that identifies one or more animation names. An animation name identifies (or selects) a CSS [**@keyframes**](/css/atrules/@keyframes) at-rule.
[**animationPlayState**](/css/properties/animation-play-state)
:   Gets or sets one or more values that specify whether an animation is playing or paused.
[**animationTimingFunction**](/css/properties/animation-timing-function)
:   Gets or sets one or more values that specify the intermediate property values to be used during a single cycle of an animation on a set of corresponding object properties identified in the CSS [**@keyframes**](/css/atrules/@keyframes) at-rule specified by the [**animationName**](/css/properties/animation-name) property.
[**backfaceVisibility**](/css/properties/backface-visibility)
:   Gets or sets a value that specifies whether the back face (reverse side) of an object is visible.
[**background**](/css/cssom/properties/background)
:   Sets or retrieves up to five separate background properties of the object.
[**backgroundAttachment**](/css/properties/background-attachment)
:   Sets or retrieves how the background image is attached to the object within the document.
[**backgroundClip**](/css/properties/background-clip)
:   Sets or retrieves the background painting area.
[**backgroundColor**](/css/properties/background-color)
:   Sets or retrieves the color behind the content of the object.
[**backgroundImage**](/css/properties/background-image)
:   Sets or retrieves the background image of the object.
[**backgroundOrigin**](/css/properties/background-origin)
:   Sets or retrieves the background positioning area of a box or multiple boxes.
[**backgroundPosition**](/css/properties/background-position)
:   Sets or retrieves the position of the background of the object.
[**backgroundPositionX**](/css/properties/background-position-x)
:   Sets or retrieves the x-coordinate of the [**background-position**](/css/properties/background-position) property.
[**backgroundPositionY**](/css/properties/background-position-y)
:   Sets or retrieves the y-coordinate of the [**background-position**](/css/properties/background-position) property.
[**backgroundRepeat**](/css/properties/background-repeat)
:   Sets or retrieves how the [**background-image**](/css/properties/background-image) property of the object is tiled.
[**backgroundSize**](/css/properties/background-size)
:   Sets or retrieves the size of the background images.
[**baselineShift**](/svg/attributes/baseline-shift)
:   Sets or retrieves a value that indicates how the dominant baseline should be repositioned relative to the dominant baseline of the parent text content element.
[**behavior**](/css/media_queries/behavior)
:   Sets or retrieves the location of the Dynamic HTML (DHTML) behavior.
[**blockDirection**](/css/cssom/styleSheet/blockDirection)
:   Gets a string value that indicates whether the content in the block element flows from left to right, or from right to left.
[**border**](/css/properties/border)
:   Sets or retrieves the properties to draw around the object.
[**borderBottom**](/css/properties/border-bottom)
:   Sets or retrieves the properties of the bottom border of the object.
[**borderBottomColor**](/css/properties/border-bottom-color)
:   Sets or retrieves the color of the bottom border of the object.
[**borderBottomLeftRadius**](/css/properties/border-bottom-left-radius)
:   Sets or retrieves one or two values that define the radii of the quarter ellipse that defines the shape of the lower-left corner for the outer border edge of the current box.
[**borderBottomRightRadius**](/css/properties/border-bottom-right-radius)
:   Sets or retrieves one or two values that define the radii of the quarter ellipse that defines the shape of the lower-right corner for the outer border edge of the current box.
[**borderBottomStyle**](/css/properties/border-bottom-style)
:   Sets or retrieves the style of the bottom border of the object.
[**borderBottomWidth**](/css/properties/border-bottom-width)
:   Sets or retrieves the width of the bottom border of the object.
[**borderCollapse**](/css/properties/border-collapse)
:   Sets or retrieves a value that indicates whether the row and cell borders of a table are joined in a single border or detached as in standard HTML.
[**borderColor**](/css/properties/border-color)
:   Sets or retrieves the border color of the object.
[**borderLeft**](/css/properties/border-left)
:   Sets or retrieves the properties of the left border of the object.
[**borderLeftColor**](/css/properties/border-left-color)
:   Sets or retrieves the color of the left border of the object.
[**borderLeftStyle**](/css/properties/border-left-style)
:   Sets or retrieves the style of the left border of the object.
[**borderLeftWidth**](/css/properties/border-left-width)
:   Sets or retrieves the width of the left border of the object.
[**borderRadius**](/css/properties/border-radius)
:   Sets or retrieves one or more values that define the radii of a quarter ellipse that defines the shape of the corners for the outer border edge of the current box.
[**borderRight**](/css/properties/border-right)
:   Sets or retrieves the properties of the right border of the object.
[**borderRightColor**](/css/properties/border-right-color)
:   Sets or retrieves the color of the right border of the object.
[**borderRightStyle**](/css/properties/border-right-style)
:   Sets or retrieves the style of the right border of the object.
[**borderRightWidth**](/css/properties/border-right-width)
:   Sets or retrieves the width of the right border of the object.
[**borderSpacing**](/css/properties/border-spacing)
:   Sets or retrieves

    the distance between the borders of adjoining cells in a table.

[**borderStyle**](/css/properties/border-style)
:   Sets or retrieves the style of the left, right, top, and bottom borders of the object.
[**borderTop**](/css/properties/border-top)
:   Sets or retrieves the properties of the top border of the object.
[**borderTopColor**](/css/properties/border-top-color)
:   Sets or retrieves the color of the top border of the object.
[**borderTopLeftRadius**](/css/properties/border-top-left-radius)
:   Sets or retrieves one or two values that define the radii of the quarter ellipse that defines the shape of the upper-left corner for the outer border edge of the current box.
[**borderTopRightRadius**](/css/properties/border-top-right-radius)
:   Sets or retrieves one or two values that define the radii of the quarter ellipse that defines the shape of the upper-right corner for the outer border edge of the current box.
[**borderTopStyle**](/css/properties/border-top-style)
:   Sets or retrieves the style of the top border of the object.
[**borderTopWidth**](/css/properties/border-top-width)
:   Sets or retrieves the width of the top border of the object.
[**borderWidth**](/css/properties/border-width)
:   Sets or retrieves the width of the left, right, top, and bottom borders of the object.
[**bottom**](/css/properties/bottom)
:   Sets or retrieves the bottom position of the object in relation to the bottom of the next positioned object in the document hierarchy.
[**boxShadow**](/css/properties/box-shadow)
:   Sets or retrieves a comma-separated list of shadows that attaches one or more drop shadows to the current box.
[**boxSizing**](/w/index.php?title=css/selectors/box-sizing&action=edit&redlink=1)
:   Sets or retrieves

    the box model to use for object sizing.

[**breakAfter**](/css/properties/break-after)
:   Gets or sets the column-break behavior that follows a content block in a multi-column element.
[**breakBefore**](/css/properties/break-before)
:   Gets or sets the column-break behavior that precedes a content block in a multi-column element.
[**breakInside**](/css/properties/break-inside)
:   Gets or sets the column-break behavior that occurs within a content block in a multi-column element.
[**captionSide**](/css/properties/caption-side)
:   Sets or retrieves

    where the **caption** of a [**table**](/html/elements/table) is located.

[**clear**](/css/properties/clear)
:   Sets or retrieves whether the object allows floating objects on its left side, right side, or both, so that the next text displays past the floating objects.
[**clip**](/css/properties/clip)
:   Sets or retrieves which part of a positioned object is visible.
[**clipBottom**](/css/cssom/properties/clipBottom)
:   Gets the bottom coordinate of the object clipping region.
[**clipLeft**](/css/cssom/properties/clipLeft)
:   Gets the left coordinate of the object clipping region.
[**clipPath**](/svg/properties/clipPath)
:   Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
[**clipRight**](/css/cssom/properties/clipRight)
:   Gets the right coordinate of the object clipping region.
[**clipTop**](/css/cssom/properties/clipTop)
:   Gets the top coordinate of the object clipping region.
[**color**](/css/properties/color)
:   Sets or retrieves the color of the text of the object.
[**columnCount**](/css/properties/column-count)
:   Gets or sets the optimal number of columns in a multi-column element.
[**columnFill**](/css/properties/column-fill)
:   Gets or sets a value that indicates how the column lengths in a multi-column element are affected by the content flow.
[**columnGap**](/css/properties/column-gap)
:   Gets or sets the width of the gap between columns in a multi-column element.
[**columnRule**](/css/properties/column-rule)
:   Gets or sets a shorthand value that specifies values for the [**columnRuleWidth**](/css/properties/column-rule-width), [**columnRuleStyle**](/css/properties/column-rule-style), and the [**columnRuleColor**](/css/properties/column-rule-color) of a multi-column element.
[**columnRuleColor**](/css/properties/column-rule-color)
:   Gets or sets the color for all column rules in a multi-column element.
[**columnRuleStyle**](/css/properties/column-rule-style)
:   Gets or sets the style for all column rules in a multi-column element.
[**columnRuleWidth**](/css/properties/column-rule-width)
:   Gets or sets the width of all column rules in a multi-column element.
[**columnSpan**](/css/properties/column-span)
:   Gets or sets the number of columns that a content block spans in a multi-column element.
[**columnWidth**](/css/properties/column-width)
:   Gets or sets the optimal width of the columns in a multi-column element.
[**constructor**](/w/index.php?title=dom/properties/constructor&action=edit&redlink=1)
:   Returns a reference to the constructor of an object.
[**content**](/css/properties/content)
:   Sets or retrieves

    generated content to insert before or after an element.

[**counterIncrement**](/css/properties/counter-increment)
:   Sets or retrieves

    a list of counters to increment.

[**counterReset**](/css/properties/counter-reset)
:   Sets or retrieves

    a list of counters to create or reset to zero.

[**cssFloat**](/css/cssom/properties/cssFloat)
:   Sets or retrieves a value that specifies whether a box should float to the left, right, or not at all.
[**cssText**](/css/cssom/styleSheet/cssText)
:   Sets or retrieves the persisted representation of the style rule.
[**cursor**](/css/selectors/cursor)
:   Sets or retrieves the type of cursor to display as the mouse pointer moves over the object.
[**direction**](/css/properties/direction)
:   Sets or retrieves the reading order of the object.
[**display**](/css/properties/display)
:   Gets or sets a value that indicates whether and how the object is rendered.
[**dominantBaseline**](/svg/attributes/dominant-baseline)
:   Sets or retrieves a value that determines or redetermines a scaled-baseline table.
[**emptyCells**](/css/properties/empty-cells)
:   Determines whether to show or hide a cell without content.
[**fill**](/svg/attributes/fill)
:   Sets or retrieves a value that indicates the color to paint the interior of the given graphical element.
[**fillOpacity**](/svg/attributes/fill-opacity)
:   Sets or retrieves a value that specifies the opacity of the painting operation that is used to paint the interior of the current object.
[**fillRule**](/svg/attributes/fill-rule)
:   Sets or retrieves a value that indicates the algorithm that is to be used to determine what parts of the canvas are included inside the shape.
[**filter**](/css/media_queries/filter)
:   Sets or retrieves the filter or collection of filters that are applied to the object.
[**font**](/css/properties/font)
:   Sets or retrieves a combination of separate [**font**](/css/properties/font) properties of the object. Alternatively, sets or retrieves one or more of six user-preference fonts.
[**fontFamily**](/css/properties/font-family)
:   Sets or retrieves the name of the font used for text in the object.
[**fontSize**](/css/properties/font-size)
:   Sets or retrieves a value that indicates the font size used for text in the object.
[**fontSizeAdjust**](/css/properties/font-size-adjust)
:   Sets or retrieves a value that specifies an aspect value for an element that will effectively preserve the x-height of the first choice font, whether it is substituted or not.
[**fontStretch**](/css/properties/font-stretch)
:   Sets or retrieves a value that indicates a normal, condensed, or expanded face of a font family.
[**fontStyle**](/css/properties/font-style)
:   Sets or retrieves the font style of the object as **italic**, **normal**, or **oblique**.
[**fontVariant**](/css/fonts/font-variant)
:   Gets or sets whether the text of the object is in small capital letters.
[**fontWeight**](/css/cssom/properties/fontWeight)
:   Gets the numeric weight of the font of the object.
[**fontWeight**](/css/properties/font-weight)
:   Gets of sets the weight of the font of the object.
[**glyphOrientationHorizontal**](/svg/attributes/glyph-orientation-horizontal)
:   Sets or retrieves a value that alters the orientation of a sequence of characters relative to an inline-progression-direction of horizontal.
[**glyphOrientationVertical**](/svg/attributes/glyph-orientation-vertical)
:   Sets or retrieves a value that alters the orientation of a sequence of characters relative to an inline-progression-direction of vertical.
[**hasLayout**](/css/cssom/properties/hasLayout)
:   Gets a value that indicates whether the object has layout.
[**height**](/css/properties/height)
:   Sets or retrieves the height of the object.
[**imeMode**](/css/properties/ime-mode)
:   Sets or retrieves the state of an IME.
[**kerning**](/svg/attributes/kerning)
:   Gets or sets a value that indicates whether Internet Explorer should adjust inter-glyph spacing based on kerning tables that are included in the relevant font (that is, enable auto-kerning) or instead disable auto-kerning and set inter-character spacing to a specific length (typically zero).

    Gets or sets a value that indicates whether the user-agent should adjust inter-glyph spacing based on kerning tables that are included in the relevant font (that is, enable auto-kerning) or instead disable auto-kerning and set inter-character spacing to a specific length (typically zero).

[**layoutFlow**](/css/properties/layout-flow)
:   Sets or retrieves the direction and flow of the content in the object.
[**layoutGrid**](/css/properties/layout-grid)
:   Sets or retrieves the composite document grid properties that specify the layout of text characters.
[**layoutGridChar**](/css/properties/layout-grid-char)
:   Sets or retrieves the size of the character grid used for rendering the text content of an element.
[**layoutGridLine**](/css/properties/layout-grid-line)
:   Sets or retrieves the gridline value used for rendering the text content of an element.
[**layoutGridMode**](/css/properties/layout-grid-mode)
:   Gets or sets whether the text layout grid uses two dimensions.
[**layoutGridType**](/css/properties/layout-grid-type)
:   Sets or retrieves the type of grid used for rendering the text content of an element.
[**left**](/css/properties/left)
:   Sets or retrieves the position of the object relative to the left edge of the next positioned object in the document hierarchy.
[**length**](/css/cssom/properties/length)
:   Retrieves the number of properties that are explicitly set on the parent object.
[**letterSpacing**](/css/properties/letter-spacing)
:   Sets or retrieves the amount of additional space between letters in the object.
[**lineBreak**](/css/properties/line-break)
:   Deprecated. Gets or sets

    line-breaking rules for text in selected languages such as Japanese, Chinese, and Korean.

[**lineHeight**](/css/properties/line-height)
:   Sets or retrieves the distance between lines in the object.
[**listStyle**](/css/properties/list-style)
:   Sets or retrieves up to three separate [**list-style**](/css/properties/list-style) properties of the object.
[**listStyleImage**](/css/properties/list-style-image)
:   Sets or retrieves a value that indicates which image to use as a list-item marker for the object.
[**listStylePosition**](/css/properties/list-style-position)
:   Sets or retrieves a variable that indicates how the list-item marker is drawn relative to the content of the object.
[**listStyleType**](/css/properties/list-style-type)
:   Sets or retrieves the predefined type of the line-item marker for the object.
[**margin**](/css/properties/margin)
:   Sets or retrieves the width of the top, right, bottom, and left margins of the object.
[**marginBottom**](/css/properties/margin-bottom)
:   Sets or retrieves the height of the bottom margin of the object.
[**marginLeft**](/css/properties/margin-left)
:   Sets or retrieves the width of the left margin of the object.
[**marginRight**](/css/properties/margin-right)
:   Sets or retrieves the width of the right margin of the object.
[**marginTop**](/css/properties/margin-top)
:   Sets or retrieves the height of the top margin of the object.
[**marker**](/svg/attributes/marker)
:   Sets or retrieves a value that specifies the marker symbol that is used for all vertices on the given [**path**](/svg/elements/path) element or basic shape.
[**markerEnd**](/svg/attributes/marker-end)
:   Sets or retrieves a value that defines the arrowhead or polymarker that is drawn at the final vertex of a given [**path**](/svg/elements/path) element or basic shape.
[**markerMid**](/svg/attributes/marker-mid)
:   Sets or retrieves a value that defines the arrowhead or polymarker that is drawn at every other vertex (that is, every vertex except the first and last) of a given [**path**](/svg/elements/path) element or basic shape.
[**markerStart**](/svg/attributes/marker-start)
:   Sets or retrieves a value that defines the arrowhead or polymarker that is drawn at the first vertex of a given [**path**](/svg/elements/path) element or basic shape.
[**mask**](/svg/attributes/mask)
:   Sets or retrieves a value that indicates a SVG mask.
[**maxHeight**](/css/properties/max-height)
:   Sets or retrieves the maximum height for an element.
[**maxWidth**](/css/properties/max-width)
:   Sets or retrieves the maximum width for an element.
[**minHeight**](/css/properties/min-height)
:   Sets or retrieves the minimum height for an element.
[**minWidth**](/css/properties/min-width)
:   Sets or retrieves the minimum width for an element.
[**msBlockProgression**](/css/properties/ms-block-progression)
:   Sets or retrieves the block progression and layout orientation.
[**msBoxAlign**](/css/properties/ms-box-align)
:   Do not use. This property has been replaced by the [**-ms-flex-align**](/css/properties/ms-flex-align) property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
[**msBoxDirection**](/css/properties/ms-box-direction)
:   Do not use. This property has been replaced by the [**-ms-flex-direction**](/css/properties/ms-flex-direction) property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
[**msBoxFlex**](/css/properties/ms-box-flex)
:   Do not use. This property has been replaced by the [**-ms-flex**](/css/properties/ms-flex) property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
[**msBoxLineProgression**](/css/properties/ms-box-line-progression)
:   Do not use. This property has been replaced by the [**-ms-flex-wrap**](/css/properties/ms-flex-wrap) property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
[**msBoxLines**](/css/properties/ms-box-lines)
:   Do not use. This property has been replaced by the [**-ms-flex-wrap**](/css/properties/ms-flex-wrap) property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
[**msBoxOrdinalGroup**](/css/properties/ms-box-ordinal-group)
:   Do not use. This property has been replaced by the [**-ms-flex-order**](/css/properties/ms-flex-order) property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
[**msBoxOrient**](/css/properties/ms-box-orient)
:   Do not use. This property has been replaced by the [**-ms-flex-direction**](/css/properties/ms-flex-direction) property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
[**msGridColumn**](/css/properties/ms-grid-column)
:   Gets or sets a value that specifies in which column of the grid to place the object.
[**msGridColumnAlign**](/w/index.php?title=css/properties/ms-grid-column-align&action=edit&redlink=1)
:   Gets or sets a value that specifies the horizontal alignment of the object within the grid column.
[**msGridColumns**](/w/index.php?title=css/properties/ms-grid-columns&action=edit&redlink=1)
:   Gets or sets one or more values that specify the width of each grid column within the object.
[**msGridColumnSpan**](/css/properties/ms-grid-column-span)
:   Gets or sets a value that specifies the number of columns of the grid that the object spans.
[**msGridRow**](/w/index.php?title=css/properties/ms-grid-row&action=edit&redlink=1)
:   Gets or sets a value that specifies in which row of the grid to place the object.
[**msGridRowAlign**](/w/index.php?title=css/properties/ms-grid-row-align&action=edit&redlink=1)
:   Gets or sets a value that specifies the vertical alignment of the object within the grid row.
[**msGridRows**](/w/index.php?title=css/properties/ms-grid-rows&action=edit&redlink=1)
:   Gets or sets one or more values that specify the height of each grid row within the object.
[**msGridRowSpan**](/w/index.php?title=css/properties/ms-grid-row-span&action=edit&redlink=1)
:   Gets or sets a value that specifies the number of rows of the grid that the object spans.
[**msInterpolationMode**](/css/media_queries/ms-interpolation-mode)
:   Obsolete. Gets or sets the interpolation (resampling) method used to stretch images.
[**msProgressAppearance**](/w/index.php?title=css/selectors/-ms-progress-appearance&action=edit&redlink=1)
:   This property is obsolete. Use [**animation-name**](/css/properties/animation-name) instead.
[**opacity**](/css/properties/opacity)
:   Gets or sets a value that specifies object or group opacity in CSS or SVG.
[**orphans**](/css/properties/orphans)
:   Sets or retrieves

    the minimum number of lines of a paragraph that must appear at the bottom of a page.

[**outline**](/css/selectors/outline)
:   Sets or retrieves

    the color, style, and width of the outline frame.

[**outlineColor**](/css/selectors/outline-color)
:   Sets or retrieves

    the color of the outline frame.

[**outlineStyle**](/css/selectors/outline-style)
:   Sets or retrieves

    the style of the outline frame.

[**outlineWidth**](/css/selectors/outline-width)
:   Sets or retrieves

    the width of the outline frame.

[**overflow**](/css/properties/overflow)
:   Sets or retrieves a value indicating how to manage the content of the object when the content exceeds the height or width of the object.
[**overflowX**](/css/properties/overflow-x)
:   Sets or retrieves how to manage the content of the object when the content exceeds the width of the object.
[**overflowY**](/css/properties/overflow-y)
:   Sets or retrieves how to manage the content of the object when the content exceeds the height of the object.
[**padding**](/css/properties/padding)
:   Sets or retrieves the amount of space to insert between the object and its margin or, if there is a border, between the object and its border.
[**paddingBottom**](/css/properties/padding-bottom)
:   Sets or retrieves the amount of space to insert between the bottom border of the object and the content.
[**paddingLeft**](/css/properties/padding-left)
:   Sets or retrieves the amount of space to insert between the left border of the object and the content.
[**paddingRight**](/css/properties/padding-right)
:   Sets or retrieves the amount of space to insert between the right border of the object and the content.
[**paddingTop**](/css/properties/padding-top)
:   Sets or retrieves the amount of space to insert between the top border of the object and the content.
[**pageBreakAfter**](/css/properties/page-break-after)
:   Sets or retrieves a value indicating whether a page break occurs after the object.
[**pageBreakBefore**](/css/properties/page-break-before)
:   Sets or retrieves a string indicating whether a page break occurs before the object.
[**pageBreakInside**](/css/properties/page-break-inside)
:   Sets or retrieves

    a string indicating whether a page break is allowed to occur inside the object.

[**parentRule**](/css/cssom/CSSRule/parentRule)
:   Retrieves the containing rule, if the current rule is contained inside another rule.
[**perspective**](/css/properties/perspective)
:   Gets or sets a value that represents the perspective from which all child elements of the object are viewed.
[**perspectiveOrigin**](/css/properties/perspective-origin)
:   Gets or sets one or two values that represent the origin (the vanishing point for the 3-D space) of an object with an [**perspective**](/css/properties/perspective) property declaration.
[**pointerEvents**](/svg/attributes/pointers)
:   Sets or retrieves a value that specifies under what circumstances a given graphics element can be the target element for a pointer event in SVG.
[**position**](/css/properties/position)
:   Sets or retrieves the type of positioning used for the object.
[**quotes**](/css/properties/quotes)
:   Sets or retrieves the pairs of strings to be used as quotes in generated content.
[**right**](/css/properties/right)
:   Sets or retrieves the position of the object relative to the right edge of the next positioned object in the document hierarchy.
[**rubyAlign**](/css/properties/ruby-align)
:   Gets or sets a value that indicates how to align the ruby text content.
[**rubyOverhang**](/css/properties/ruby-overhang)
:   Gets or sets a value that indicates whether, and on which side, ruby text is allowed to partially overhang any adjacent text in addition to its own base, when the ruby text is wider than the ruby base
[**rubyPosition**](/css/properties/ruby-position)
:   Gets or sets a value that controls the position of the ruby text with respect to its base.
[**scrollbar3dLightColor**](/w/index.php?title=css/selectors/-ms-scrollbar-3d-light-color&action=edit&redlink=1)
:   Sets or retrieves the color of the top and left edges of the scroll box and scroll arrows of a scroll bar.
[**scrollbarArrowColor**](/w/index.php?title=css/selectors/-ms-scrollbar-arrow-color&action=edit&redlink=1)
:   Sets or retrieves the color of the arrow elements of a scroll arrow.
[**scrollbarBaseColor**](/w/index.php?title=css/selectors/-ms-scrollbar-base-color&action=edit&redlink=1)
:   Sets or retrieves the color of the main elements of a scroll bar, which include the scroll box, track, and scroll arrows.
[**scrollbarDarkShadowColor**](/w/index.php?title=css/selectors/-ms-scrollbar-darkshadow-color&action=edit&redlink=1)
:   Sets or retrieves the color of the gutter of a scroll bar.
[**scrollbarFaceColor**](/w/index.php?title=css/selectors/-ms-scrollbar-face-color&action=edit&redlink=1)
:   Sets or retrieves the color of the scroll box and scroll arrows of a scroll bar.
[**scrollbarHighlightColor**](/w/index.php?title=css/selectors/-ms-scrollbar-highlight-color&action=edit&redlink=1)
:   Sets or retrieves the color of the top and left edges of the scroll box and scroll arrows of a scroll bar.
[**scrollbarShadowColor**](/css/selectors/-ms-scrollbar-shadow-color)
:   Sets or retrieves the color of the bottom and right edges of the scroll box and scroll arrows of a scroll bar.
[**scrollbarTrackColor**](/w/index.php?title=css/selectors/-ms-scrollbar-track-color&action=edit&redlink=1)
:   Sets or retrieves the color of the track element of a scroll bar.
[**stopColor**](/svg/attributes/stop-color)
:   Sets or retrieves a value that indicates what color to use at the current gradient stop.
[**stopOpacity**](/svg/attributes/stop-opacity)
:   Sets or retrieves a value that defines the opacity of the current gradient stop.
[**stroke**](/svg/attributes/stroke)
:   Sets or retrieves a value that indicates the color to paint along the outline of a given graphical element.
[**strokeDasharray**](/svg/attributes/stroke-dasharray)
:   Sets or retrieves one or more values that indicate the pattern of dashes and gaps used to stroke paths.
[**strokeDashoffset**](/svg/attributes/stroke-dashoffset)
:   Sets or retrieves a value that specifies the distance into the dash pattern to start the dash.
[**strokeLinecap**](/svg/attributes/stroke-linecap)
:   Sets or retrieves a value that specifies the shape to be used at the end of open subpaths when they are stroked.
[**strokeLinejoin**](/svg/attributes/stroke-linejoin)
:   Sets or retrieves a value that specifies the shape to be used at the corners of paths or basic shapes when they are stroked.
[**strokeMiterlimit**](/svg/attributes/stroke-miterlimit)
:   Sets or retrieves a value that indicates the limit on the ratio of the length of miter joins (as specified in the [**strokeLinejoin**](/svg/attributes/stroke-linejoin) property).
[**strokeOpacity**](/svg/attributes/stroke-opacity)
:   Sets or retrieves a value that specifies the opacity of the painting operation that is used to stroke the current object.
[**strokeWidth**](/svg/attributes/stroke-width)
:   Sets or retrieves a value that specifies the width of the stroke on the current object.
[**styleFloat**](/css/properties/float)
:   Sets or retrieves on which side of the object the text will flow.
[**tableLayout**](/css/properties/table-layout)
:   Sets or retrieves a string that indicates whether the table layout is fixed.
[**textAlign**](/css/properties/text-align)
:   Sets or retrieves whether the text in the object is left-aligned, right-aligned, centered, or justified.
[**textAlignLast**](/css/properties/text-align-last)
:   Gets or sets a value that indicates how to align the last line or only line of text in the specified object.
[**textAutospace**](/css/properties/text-autospace)
:   Sets or retrieves the autospacing and narrow space width adjustment of text.
[**textDecoration**](/css/properties/text-decoration)
:   Sets or retrieves a value that indicates whether the text in the object has blink, line-through, overline, or underline decorations.
[**textIndent**](/css/properties/text-indent)
:   Sets or retrieves the indentation of the first line of text in the object.
[**textJustify**](/css/properties/text-justify)
:   Sets or retrieves the type of alignment used to justify text in the object.
[**textKashidaSpace**](/css/properties/text-kashida-space)
:   Sets or retrieves the ratio of kashida expansion to white space expansion when justifying lines of text in the object.
[**textOverflow**](/css/properties/text-overflow)
:   Sets or retrieves a value that indicates whether to render ellipses (...) to indicate text overflow.
[**textTransform**](/css/properties/text-transform)
:   Sets or retrieves the rendering of the text in the object.
[**textUnderlinePosition**](/css/properties/text-underline-position)
:   Sets or retrieves the position of the underline decoration that is set through the [**text-decoration**](/css/properties/text-decoration) property of the object.
[**top**](/css/properties/top)
:   Sets or retrieves the position of the object relative to the top of the next positioned object in the document hierarchy.
[**transform**](/css/transforms/transform)
:   Gets or sets a list of one or more transform functions that specify how to translate, rotate, or scale an element in 2-D or 3-D space.
[**transformOrigin**](/css/properties/transform-origin)
:   Gets or sets one or two values that establish the origin of transformation for an element.
[**transformStyle**](/css/properties/transform-style)
:   Gets or sets a value that specifies how child elements of the object are rendered in 3-D space.
[**transition**](/css/properties/transition)
:   Gets or sets one or more shorthand values that specify the transition properties for a set of corresponding object properties identified in the [**transition-property**](/css/properties/transition-property) property.
[**transitionDelay**](/css/properties/transition-delay)
:   Gets or sets one or more values that specify the offset within a transition (the amount of time from the start of a transition) before the transition is displayed for a set of corresponding object properties identified in the [**transition-property**](/css/properties/transition-property) property.
[**transitionDuration**](/css/properties/transition-duration)
:   Gets or sets one or more values that specify the durations of transitions on a set of corresponding object properties identified in the [**transition-property**](/css/properties/transition-property) property.
[**transitionProperty**](/css/properties/transition-property)
:   Gets or sets a value that identifies the CSS property name or names to which the transition effect (defined by [**transition-duration**](/css/properties/transition-duration), [**transition-timing-function**](/css/functions/transition-timing-function), and [**transition-delay**](/css/properties/transition-delay)) is applied when a new property value is specified.
[**transitionTimingFunction**](/css/functions/transition-timing-function)
:   Gets or sets one or more values that specify the intermediate property values to be used during a transition on a set of corresponding object properties identified in the [**transition-property**](/css/properties/transition-property) property.
[**unicodeBidi**](/css/properties/unicode-bidi)
:   Sets or retrieves the level of embedding with respect to the bidirectional algorithm.
[**verticalAlign**](/css/properties/vertical-align)
:   Sets or retrieves the vertical alignment of the object.
[**visibility**](/css/properties/visibility)
:   Sets or retrieves whether the content of the object is displayed.
[**whiteSpace**](/css/properties/white-space)
:   Sets or retrieves a value that indicates whether lines are automatically broken inside the object.
[**widows**](/css/properties/widows)
:   Sets or retrieves

    the minimum number of lines of a paragraph that must appear at the top of a document.

[**width**](/css/properties/width)
:   Sets or retrieves the width of the object.
[**wordBreak**](/css/properties/word-break)
:   Sets or retrieves

    line-breaking behavior within words, particularly where multiple languages appear in the object.

[**wordSpacing**](/css/text/word-spacing/word-spacing)
:   Sets or retrieves the amount of additional space between words in the object.
[**wordWrap**](/css/properties/word-wrap)
:   Sets or retrieves whether to break words when the content exceeds the boundaries of its container.
[**writingMode**](/css/properties/writing-mode)
:   Sets or retrieves the direction and flow of the content in the object.
[**zIndex**](/css/properties/z-index)
:   Sets or retrieves the stacking order of positioned objects.
[**zoom**](/css/selectors/zoom)
:   Sets or retrieves the magnification scale of the object.

## See also

### Related pages (MSDN)

-   `style`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

