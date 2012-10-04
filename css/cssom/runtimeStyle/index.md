{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example sets a value on the '''runtimeStyle''' object to affect the [[css/cssom/currentStyle|'''currentStyle''']] object, but not the [[css/cssom/style|'''style''']] object.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/runtimeStyle.htm
|Code=
&lt;SCRIPT&gt;
function fnChangeValue(sValue){
   if(oDIV.runtimeStyle.backgroundColor {{=}}{{=}} oDIV.style.backgroundColor){
      sValue{{=}}"";
   }
   oDIV.runtimeStyle.backgroundColor {{=}} sValue;
   console.log(oDIV.style.backgroundColor +
      "\n" + oDIV.currentStyle.backgroundColor +
      "\n" + oDIV.runtimeStyle.backgroundColor);
}
&lt;/SCRIPT&gt;
&lt;DIV ID {{=}} "oDIV"&gt;
This is a demonstration DIV.
&lt;/DIV&gt;
&lt;INPUT TYPE {{=}} "button" VALUE {{=}} "Change Color" onclick{{=}}"fnChangeValue('blue')"&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''runtimeStyle''' object sets and retrieves the format and style of an object, and overrides existing formats and styles in the process. Other than having precedence over the [[css/cssom/style|'''style''']] object and not persisting, the '''runtimeStyle''' object is equivalent to the '''style''' object.
To change or clear multiple style properties simultaneously, use this object with the [[css/cssom/styleSheet/cssText|'''cssText''']] property. For example, to change the font color and background color of a '''DIV''' element, you could use the following code:
 <code>
 &lt;DIV onclick{{=}}"this.runtimeStyle.cssText {{=}} 'color:red;background-color:blue;border:5px solid black;'"&gt;
 Click this DIV to change style properties.&lt;/DIV&gt;
 </code>
Windows Internet Explorer 8 or later. The behavior of [[dom/methods/setAttribute|'''setAttribute''']] method depends on the current document compatibility mode. For more information, see Attribute Differences in Internet Explorer 8
|Import_Notes=
===Standards information===
There are no standards that apply here.

===Members===
The '''runtimeStyle''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''runtimeStyle''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[dom/methods/getAttribute|'''getAttribute''']]
|Retrieves the value of the specified attribute.
|-
|[[css/cssom/methods/getExpression|'''getExpression''']]
|Retrieves the expression for the given property.
|-
|[[dom/methods/removeAttribute|'''removeAttribute''']]
|Removes an attribute from an object.
|-
|[[css/cssom/methods/removeExpression|'''removeExpression''']]
|Removes the expression from the specified property.
|-
|[[dom/methods/setAttribute|'''setAttribute''']]
|Sets the value of the specified attribute.
|-
|[[css/cssom/methods/setExpression|'''setExpression''']]
|Sets an expression for the specified object.
|}
 

====Properties====
The '''runtimeStyle''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[css/media queries/accelerator|'''accelerator''']]
|Sets or retrieves a string that indicates whether the object represents a keyboard shortcut.
|-
|[[css/cssom/properties/background|'''background''']]
|Sets or retrieves up to five separate background properties of the object.
|-
|[[css/properties/background-attachment|'''backgroundAttachment''']]
|Sets or retrieves  how the background image is attached to the object within the document.
|-
|[[css/properties/background-clip|'''backgroundClip''']]
|Sets or retrieves the background painting area.
|-
|[[css/properties/background-color|'''backgroundColor''']]
|Sets or retrieves  the color behind the content of the object.
|-
|[[css/properties/background-image|'''backgroundImage''']]
|Sets or retrieves  the background image of the object.
|-
|[[css/properties/background-origin|'''backgroundOrigin''']]
|Sets or retrieves the background positioning area of a box or multiple boxes.
|-
|[[css/properties/background-position|'''backgroundPosition''']]
|Sets or retrieves the position of the background of the object.
|-
|[[css/properties/background-position-x|'''backgroundPositionX''']]
|Sets or retrieves  the x-coordinate of the [[css/properties/background-position|'''background-position''']] property.
|-
|[[css/properties/background-position-y|'''backgroundPositionY''']]
|Sets or retrieves  the y-coordinate of the [[css/properties/background-position|'''background-position''']] property.
|-
|[[css/properties/background-repeat|'''backgroundRepeat''']]
|Sets or retrieves  how the [[css/properties/background-image|'''background-image''']] property of the object is tiled.
|-
|[[css/properties/background-size|'''backgroundSize''']]
|Sets or retrieves the size of the background images.
|-
|[[css/media queries/behavior|'''behavior''']]
|Sets or retrieves  the location of the Dynamic HTML (DHTML) behavior.
|-
|[[css/properties/border|'''border''']]
|Sets or retrieves the properties to draw around the object.
|-
|[[css/properties/border-bottom|'''borderBottom''']]
|Sets or retrieves the properties of the bottom border of the object.
|-
|[[css/properties/border-bottom-color|'''borderBottomColor''']]
|Sets or retrieves  the color of the bottom border of the object.
|-
|[[css/properties/border-bottom-left-radius|'''borderBottomLeftRadius''']]
|Sets or retrieves one or two values that define the radii of the quarter ellipse that defines the shape of the lower-left corner for the outer border edge of the current box.
|-
|[[css/properties/border-bottom-right-radius|'''borderBottomRightRadius''']]
|Sets or retrieves one or two values that define the radii of the quarter ellipse that defines the shape of the lower-right corner for the outer border edge of the current box.
|-
|[[css/properties/border-bottom-style|'''borderBottomStyle''']]
|Sets or retrieves  the style of the bottom border of the object.
|-
|[[css/properties/border-bottom-width|'''borderBottomWidth''']]
|Sets or retrieves  the width of the bottom border of the object.
|-
|[[css/properties/border-collapse|'''borderCollapse''']]
|Sets or retrieves  a value that indicates whether the row and cell borders of a table are joined in a single border or detached as in standard HTML.
|-
|[[css/properties/border-color|'''borderColor''']]
|Sets or retrieves  the border color of the object.
|-
|[[css/properties/border-left|'''borderLeft''']]
|Sets or retrieves the properties of the left border of the object.
|-
|[[css/properties/border-left-color|'''borderLeftColor''']]
|Sets or retrieves  the color of the left border of the object.
|-
|[[css/properties/border-left-style|'''borderLeftStyle''']]
|Sets or retrieves  the style of the left border of the object.
|-
|[[css/properties/border-left-width|'''borderLeftWidth''']]
|Sets or retrieves  the width of the left border of the object.
|-
|[[css/properties/border-radius|'''borderRadius''']]
|Sets or retrieves one or more values that define the radii of a quarter ellipse that defines the shape of the corners for the outer border edge of the current box.
|-
|[[css/properties/border-right|'''borderRight''']]
|Sets or retrieves the properties of the right border of the object.
|-
|[[css/properties/border-right-color|'''borderRightColor''']]
|Sets or retrieves  the color of the right border of the object.
|-
|[[css/properties/border-right-style|'''borderRightStyle''']]
|Sets or retrieves  the style of the right border of the object.
|-
|[[css/properties/border-right-width|'''borderRightWidth''']]
|Sets or retrieves  the width of the right border of the object.
|-
|[[css/properties/border-spacing|'''borderSpacing''']]
|Sets or retrieves 
the distance between the borders of adjoining cells in a table.
|-
|[[css/properties/border-style|'''borderStyle''']]
|Sets or retrieves  the style of the left, right, top, and bottom borders of the object.
|-
|[[css/properties/border-top|'''borderTop''']]
|Sets or retrieves the properties of the top border of the object.
|-
|[[css/properties/border-top-color|'''borderTopColor''']]
|Sets or retrieves  the color of the top border of the object.
|-
|[[css/properties/border-top-left-radius|'''borderTopLeftRadius''']]
|Sets or retrieves one or two values that define the radii of the quarter ellipse that defines the shape of the upper-left corner for the outer border edge of the current box.
|-
|[[css/properties/border-top-right-radius|'''borderTopRightRadius''']]
|Sets or retrieves one or two values that define the radii of the quarter ellipse that defines the shape of the upper-right corner for the outer border edge of the current box.
|-
|[[css/properties/border-top-style|'''borderTopStyle''']]
|Sets or retrieves  the style of the top border of the object.
|-
|[[css/properties/border-top-width|'''borderTopWidth''']]
|Sets or retrieves  the width of the top border of the object.
|-
|[[css/properties/border-width|'''borderWidth''']]
|Sets or retrieves  the width of the left, right, top, and bottom borders of the object.
|-
|[[css/properties/bottom|'''bottom''']]
|Sets or retrieves  the bottom position of the object in relation to the bottom of the next positioned object in the document hierarchy.
|-
|[[css/properties/box-shadow|'''boxShadow''']]
|Sets or retrieves a comma-separated list of shadows that attaches one or more drop shadows to the current box.
|-
|[[css/selectors/box-sizing|'''boxSizing''']]
|Sets or retrieves 
the box model to use for object sizing.
|-
|[[css/properties/caption-side|'''captionSide''']]
|Sets or retrieves 
where the '''caption'''
of a [[html/elements/table|'''table''']] is located.
|-
|[[css/properties/clear|'''clear''']]
|Sets or retrieves  whether the object allows floating objects on its left side, right side, or both, so that the next text displays past the floating objects.
|-
|[[css/properties/clip|'''clip''']]
|Sets or retrieves which part of a positioned object is visible.
|-
|[[css/properties/color|'''color''']]
|Sets or retrieves  the color of the text of the object.
|-
|[[css/properties/content|'''content''']]
|Sets or retrieves 
generated content to insert before or after an element.
|-
|[[css/properties/counter-increment|'''counterIncrement''']]
|Sets or retrieves 
a list of counters to increment.
|-
|[[css/properties/counter-reset|'''counterReset''']]
|Sets or retrieves 
a list of counters to create or reset to zero.
|-
|[[css/cssom/styleSheet/cssText|'''cssText''']]
|Sets or retrieves the persisted representation of the style rule.
|-
|[[css/selectors/cursor|'''cursor''']]
|Sets or retrieves  the type of cursor to display as the mouse pointer moves over the object.
|-
|[[css/properties/direction|'''direction''']]
|Sets or retrieves  the reading order of the object.
|-
|[[css/properties/empty-cells|'''emptyCells''']]
|Determines whether to show or hide a cell without content.
|-
|[[css/properties/font|'''font''']]
|Sets or retrieves a combination of separate [[css/properties/font|'''font''']] properties of the object. Alternatively, sets or retrieves one or more of six user-preference fonts.
|-
|[[css/properties/font-family|'''fontFamily''']]
|Sets or retrieves  the name of the font used for text in the object.
|-
|[[css/properties/font-size|'''fontSize''']]
|Sets or retrieves  a value that indicates the font size used for text in the object.
|-
|[[css/properties/font-size-adjust|'''fontSizeAdjust''']]
|Sets or retrieves a value that specifies an aspect value for an element that will effectively preserve the x-height of the first choice font, whether it is substituted or not.
|-
|[[css/properties/font-stretch|'''fontStretch''']]
|Sets or retrieves a value that indicates a normal, condensed, or expanded face of a font family.
|-
|[[css/properties/font-style|'''fontStyle''']]
|Sets or retrieves  the font style of the object as '''italic''', '''normal''', or '''oblique'''.
|-
|[[css/fonts/font-variant|'''fontVariant''']]
|Gets or sets  whether the text of the object is in small capital letters.
|-
|[[css/properties/font-weight|'''fontWeight''']]
|Gets of sets  the weight of the font of the object.
|-
|[[css/properties/height|'''height''']]
|Sets or retrieves  the height of the object.
|-
|[[css/properties/ime-mode|'''imeMode''']]
|Sets or retrieves the state of an IME.
|-
|[[css/properties/layout-flow|'''layoutFlow''']]
|Sets or retrieves  the direction and flow of the content in the object.
|-
|[[css/properties/layout-grid|'''layoutGrid''']]
|Sets or retrieves the composite document grid properties that specify the layout of text characters.
|-
|[[css/properties/layout-grid-char|'''layoutGridChar''']]
|Sets or retrieves  the size of the character grid used for rendering the text content of an element.
|-
|[[css/properties/layout-grid-line|'''layoutGridLine''']]
|Sets or retrieves  the gridline value used for rendering the text content of an element.
|-
|[[css/properties/layout-grid-mode|'''layoutGridMode''']]
|Gets or sets  whether the text layout grid uses two dimensions.
|-
|[[css/properties/layout-grid-type|'''layoutGridType''']]
|Sets or retrieves  the type of grid used for rendering the text content of an element.
|-
|[[css/properties/left|'''left''']]
|Sets or retrieves  the position of the object relative to the left edge of the next positioned object in the document hierarchy.
|-
|[[css/properties/letter-spacing|'''letterSpacing''']]
|Sets or retrieves  the amount of additional space between letters in the object.
|-
|[[css/properties/line-break|'''lineBreak''']]
|Deprecated. Gets or sets 
line-breaking rules for text in selected languages
such as Japanese, Chinese, and Korean.
|-
|[[css/properties/line-height|'''lineHeight''']]
|Sets or retrieves  the distance between lines in the object.
|-
|[[css/properties/list-style|'''listStyle''']]
|Sets or retrieves up to three separate [[css/properties/list-style|'''list-style''']] properties of the object.
|-
|[[css/properties/list-style-image|'''listStyleImage''']]
|Sets or retrieves  a value that indicates which image to use as a list-item marker for the object.
|-
|[[css/properties/list-style-position|'''listStylePosition''']]
|Sets or retrieves  a variable that indicates how the list-item marker is drawn relative to the content of the object.
|-
|[[css/properties/list-style-type|'''listStyleType''']]
|Sets or retrieves  the predefined type of the line-item marker for the object.
|-
|[[css/properties/margin|'''margin''']]
|Sets or retrieves  the width of the top, right, bottom, and left margins of the object.
|-
|[[css/properties/margin-bottom|'''marginBottom''']]
|Sets or retrieves  the height of the bottom margin of the object.
|-
|[[css/properties/margin-left|'''marginLeft''']]
|Sets or retrieves  the width of the left margin of the object.
|-
|[[css/properties/margin-right|'''marginRight''']]
|Sets or retrieves  the width of the right margin of the object.
|-
|[[css/properties/margin-top|'''marginTop''']]
|Sets or retrieves  the height of the top margin of the object.
|-
|[[css/properties/max-height|'''maxHeight''']]
|Sets or retrieves the maximum height for an element.
|-
|[[css/properties/max-width|'''maxWidth''']]
|Sets or retrieves the maximum width for an element.
|-
|[[css/properties/min-height|'''minHeight''']]
|Sets or retrieves the minimum height for an element.
|-
|[[css/properties/min-width|'''minWidth''']]
|Sets or retrieves the minimum width for an element.
|-
|[[css/properties/ms-block-progression|'''msBlockProgression''']]
|Sets or retrieves the block progression and layout orientation.
|-
|[[css/media queries/ms-interpolation-mode|'''msInterpolationMode''']]
|Obsolete. Gets or sets the interpolation (resampling) method used to stretch images.
|-
|[[css/selectors/-ms-progress-appearance|'''msProgressAppearance''']]
|This property is obsolete. Use [[css/properties/animation-name|'''animation-name''']] instead.
|-
|[[css/properties/opacity|'''opacity''']]
|Gets or sets a value that specifies object or group opacity in CSS or SVG.
|-
|[[css/properties/orphans|'''orphans''']]
|Sets or retrieves 
the minimum number of lines of a paragraph that must appear
at the bottom of a page.
|-
|[[css/selectors/outline|'''outline''']]
|Sets or retrieves 
the color, style, and width of the outline frame.
|-
|[[css/selectors/outline-color|'''outlineColor''']]
|Sets or retrieves 
the color of the outline frame.
|-
|[[css/selectors/outline-style|'''outlineStyle''']]
|Sets or retrieves 
the style of the outline frame.
|-
|[[css/selectors/outline-width|'''outlineWidth''']]
|Sets or retrieves 
the width of the outline frame.
|-
|[[css/properties/overflow|'''overflow''']]
|Sets or retrieves  a value indicating how to manage the content of the object when the content exceeds the height or width of the object.
|-
|[[css/properties/overflow-x|'''overflowX''']]
|Sets or retrieves  how to manage the content of the object when the content exceeds the width of the object.
|-
|[[css/properties/overflow-y|'''overflowY''']]
|Sets or retrieves  how to manage the content of the object when the content exceeds the height of the object.
|-
|[[css/properties/padding|'''padding''']]
|Sets or retrieves the amount of space to insert between the object and its margin or, if there is a border, between the object and its border.
|-
|[[css/properties/padding-bottom|'''paddingBottom''']]
|Sets or retrieves  the amount of space to insert between the bottom border of the object and the content.
|-
|[[css/properties/padding-left|'''paddingLeft''']]
|Sets or retrieves  the amount of space to insert between the left border of the object and the content.
|-
|[[css/properties/padding-right|'''paddingRight''']]
|Sets or retrieves  the amount of space to insert between the right border of the object and the content.
|-
|[[css/properties/padding-top|'''paddingTop''']]
|Sets or retrieves  the amount of space to insert between the top border of the object and the content.
|-
|[[css/properties/page-break-after|'''pageBreakAfter''']]
|Sets or retrieves  a value indicating whether a page break occurs after the object.
|-
|[[css/properties/page-break-before|'''pageBreakBefore''']]
|Sets or retrieves  a string indicating whether a page break occurs before the object.
|-
|[[css/properties/page-break-inside|'''pageBreakInside''']]
|Sets or retrieves 
a string indicating whether a page break is allowed to occur inside the
object.
|-
|[[css/cssom/properties/pixelBottom|'''pixelBottom''']]
|Sets or retrieves the bottom position of the object.
|-
|[[css/cssom/properties/pixelHeight|'''pixelHeight''']]
|Sets or retrieves the height of the object.
|-
|[[css/cssom/properties/pixelLeft|'''pixelLeft''']]
|Sets or retrieves the left position of the object.
|-
|[[css/cssom/properties/pixelRight|'''pixelRight''']]
|Sets or retrieves the right position of the object.
|-
|[[css/cssom/properties/pixelTop|'''pixelTop''']]
|Sets or retrieves the top position of the object.
|-
|[[css/cssom/properties/pixelWidth|'''pixelWidth''']]
|Sets or retrieves the width of the object.
|-
|[[css/cssom/properties/posBottom|'''posBottom''']]
|Sets or retrieves the bottom position of the object in the units specified by the [[css/properties/bottom|'''bottom''']] attribute.
|-
|[[css/cssom/properties/posHeight|'''posHeight''']]
|Sets or retrieves the height of the object in the units specified by the [[css/properties/height|'''height''']] attribute.
|-
|[[css/properties/position|'''position''']]
|Sets or retrieves  the type of positioning used for the object.
|-
|[[css/cssom/properties/posLeft|'''posLeft''']]
|Sets or retrieves the left position of the object in the units specified by the [[css/properties/left|'''left''']] attribute.
|-
|[[css/cssom/properties/posRight|'''posRight''']]
|Sets or retrieves the right position of the object in the units specified by the [[css/properties/right|'''right''']] attribute.
|-
|[[css/cssom/properties/posTop|'''posTop''']]
|Sets or retrieves the top position of the object in the units specified by the [[css/properties/top|'''top''']] attribute.
|-
|[[css/cssom/properties/posWidth|'''posWidth''']]
|Sets or retrieves the width of the object in the units specified by the [[css/properties/width|'''width''']] attribute.
|-
|[[css/properties/quotes|'''quotes''']]
|Sets or retrieves  the pairs of strings to be used as quotes in generated content.
|-
|[[css/properties/right|'''right''']]
|Sets or retrieves  the position of the object relative to the right edge of the next positioned object in the document hierarchy.
|-
|[[css/properties/ruby-align|'''rubyAlign''']]
|Gets or sets a value that indicates  how to align the ruby text content.
|-
|[[css/properties/ruby-overhang|'''rubyOverhang''']]
|Gets or sets a value that indicates  whether, and on which side, ruby text is allowed to partially overhang any adjacent text in addition to its own base, when the ruby text is wider than the ruby base
|-
|[[css/properties/ruby-position|'''rubyPosition''']]
|Gets or sets  a value that controls the position of the ruby text with respect to its base.
|-
|[[css/selectors/-ms-scrollbar-3d-light-color|'''scrollbar3dLightColor''']]
|Sets or retrieves the color of the top and left edges of the scroll box and scroll arrows of a scroll bar.
|-
|[[css/selectors/-ms-scrollbar-arrow-color|'''scrollbarArrowColor''']]
|Sets or retrieves the color of the arrow elements of a scroll arrow.
|-
|[[css/selectors/-ms-scrollbar-base-color|'''scrollbarBaseColor''']]
|Sets or retrieves the color of the main elements of a scroll bar, which include the scroll box, track, and scroll arrows.
|-
|[[css/selectors/-ms-scrollbar-darkshadow-color|'''scrollbarDarkShadowColor''']]
|Sets or retrieves the color of the gutter of a scroll bar.
|-
|[[css/selectors/-ms-scrollbar-face-color|'''scrollbarFaceColor''']]
|Sets or retrieves the color of the scroll box and scroll arrows of a scroll bar.
|-
|[[css/selectors/-ms-scrollbar-highlight-color|'''scrollbarHighlightColor''']]
|Sets or retrieves the color of the top and left edges of the scroll box and scroll arrows of a scroll bar.
|-
|[[css/selectors/-ms-scrollbar-shadow-color|'''scrollbarShadowColor''']]
|Sets or retrieves the color of the bottom and right edges of the scroll box and scroll arrows of a scroll bar.
|-
|[[css/selectors/-ms-scrollbar-track-color|'''scrollbarTrackColor''']]
|Sets or retrieves the color of the track element of a scroll bar.
|-
|[[css/properties/float|'''styleFloat''']]
|Sets or retrieves  on which side of the object the text will flow.
|-
|[[css/properties/table-layout|'''tableLayout''']]
|Sets or retrieves  a string that indicates whether the table layout is fixed.
|-
|[[css/properties/text-align|'''textAlign''']]
|Sets or retrieves  whether the text in the object is left-aligned, right-aligned, centered, or justified.
|-
|[[css/properties/text-align-last|'''textAlignLast''']]
|Gets or sets a value that indicates  how to align the last line or only line of text in the specified object.
|-
|[[css/properties/text-autospace|'''textAutospace''']]
|Sets or retrieves  the autospacing and narrow space width adjustment of text.
|-
|[[css/properties/text-decoration|'''textDecoration''']]
|Sets or retrieves  a value that indicates whether the text in the object has blink, line-through, overline, or underline decorations.
|-
|[[css/properties/text-decoration-blink|'''textDecorationBlink''']]
|Sets or retrieves a Boolean value that indicates whether the object's [[css/properties/text-decoration|'''textDecoration''']] property has a value of "blink."



This property is not supported for Metro style apps using JavaScript.
|-
|[[css/properties/text-decoration-line-through|'''textDecorationLineThrough''']]
|Sets or retrieves a Boolean value indicating whether the text in the object has a line drawn through it.
|-
|[[css/properties/text-decoration-none|'''textDecorationNone''']]
|Sets or retrieves the Boolean value indicating whether the [[css/properties/text-decoration|'''textDecoration''']] property for the object has been set to '''none'''.
|-
|[[css/properties/text-decoration-overline|'''textDecorationOverline''']]
|Sets or retrieves a Boolean value indicating whether the text in the object has a line drawn over it.
|-
|[[css/properties/text-decoration-underline|'''textDecorationUnderline''']]
|Sets or retrieves whether the text in the object is underlined.
|-
|[[css/properties/text-indent|'''textIndent''']]
|Sets or retrieves  the indentation of the first line of text in the object. 

This property is not supported for Metro style apps using JavaScript.
|-
|[[css/properties/text-justify|'''textJustify''']]
|Sets or retrieves  the type of alignment used to justify text in the object.
|-
|[[css/properties/text-kashida-space|'''textKashidaSpace''']]
|Sets or retrieves  the ratio of kashida expansion to white space expansion when justifying lines of text in the object.
|-
|[[css/properties/text-overflow|'''textOverflow''']]
|Sets or retrieves a value that indicates whether to render ellipses (...) to indicate text overflow.
|-
|[[css/properties/text-transform|'''textTransform''']]
|Sets or retrieves  the rendering of the text in the object.
|-
|[[css/properties/text-underline-position|'''textUnderlinePosition''']]
|Sets or retrieves  the position of the underline decoration that is set through the  [[css/properties/text-decoration|'''text-decoration''']] property of the object.
|-
|[[css/properties/top|'''top''']]
|Sets or retrieves  the position of the object relative to the top of the next positioned object in the document hierarchy.
|-
|[[css/properties/unicode-bidi|'''unicodeBidi''']]
|Sets or retrieves  the level of embedding with respect to the bidirectional algorithm.
|-
|[[css/properties/vertical-align|'''verticalAlign''']]
|Sets or retrieves  the vertical alignment of the object.
|-
|[[css/properties/visibility|'''visibility''']]
|Sets or retrieves  whether the content of the object is displayed.
|-
|[[css/properties/widows|'''widows''']]
|Sets or retrieves 
the minimum number of lines of a paragraph that must appear
at the top of a document.
|-
|[[css/properties/width|'''width''']]
|Sets or retrieves  the width of the object.
|-
|[[css/properties/word-break|'''wordBreak''']]
|Sets or retrieves
line-breaking behavior within words, particularly where multiple
languages appear in the object.
|-
|[[css/text/word-spacing/word-spacing|'''wordSpacing''']]
|Sets or retrieves the amount of additional space between words in the object.
|-
|[[css/properties/word-wrap|'''wordWrap''']]
|Sets or retrieves  whether to break words when the content exceeds the boundaries of its container.
|-
|[[css/properties/writing-mode|'''writingMode''']]
|Sets or retrieves  the direction and flow of the content in the object.
|-
|[[css/properties/z-index|'''zIndex''']]
|Sets or retrieves  the stacking order of positioned objects.
|-
|[[css/selectors/zoom|'''zoom''']]
|Sets or retrieves  the magnification scale of the object.
|}
 

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
|Topic_clusters=CSSOM
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}