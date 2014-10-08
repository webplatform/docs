{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=summary needed. double check token printing in standards section.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section}}
{{API_Object
|Subclass_of=
|Overview=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
|Description=This example uses the '''style''' object to set the document body text font to Verdana.
|Code=document.body.style.fontFamily {{=}} "Verdana"
|LiveURL=
}}{{Single Example
|Language=
|Description=This example positions all absolutely positioned images in the given document at the top of the document.
|Code=var oImages {{=}} document.all.tags("IMG");
if (oImages.length) {
    for (var iImg {{=}} 0; iImg &lt; oImages.length; iImg++) {
        var oImg {{=}} oImages(iImg);
        if (oImg.style.position {{=}}{{=}} "absolute") {
            oImg.style.top {{=}} 0;
        }
    }
}
|LiveURL=
}}{{Single Example
|Language=
|Description=This example copies the inline style of the second element (<code>div2</code>) to the first (<code>div1</code>) while preserving the styles of the second. The background color of <code>div1</code> is overwritten during the assignment.
|Code=&lt;DIV ID{{=}}"div1" STYLE{{=}}"background-color:blue;font-weight:bold"&gt;Item 1&lt;/DIV&gt;
&lt;DIV ID{{=}}"div2" STYLE{{=}}"background-color:red;font-size:18pt;
    font-family:Verdana;"&gt;Item 2&lt;/DIV&gt;
&lt;SCRIPT&gt;
div1.style.cssText +{{=}} (';' + div2.style.cssText);
&lt;/SCRIPT&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
Inline styles are CSS assignments that you apply directly to individual HTML elements using the [[html/attributes/STYLE html_attribute|'''STYLE''']] attribute. Use the '''style''' object to examine these assignments and to make new assignments or change existing ones.
To retrieve the '''style''' object, apply the '''style''' keyword to an <code>element</code> object. To retrieve the current setting for an inline style, apply the corresponding '''style''' property to the '''style''' object.
The '''style''' object does not provide access to the style assignments in style sheets. To obtain information about styles in style sheets, use the [[css/cssom/styleSheets|'''styleSheets''']] collection to access to the individual style sheets defined in the document.
The following properties are not available when the [[css/cssom/rule|'''rule''']] object accesses the '''style''' object: [[css/cssom/properties/posHeight|'''posHeight''']], [[css/cssom/properties/posWidth|'''posWidth''']], [[css/cssom/properties/posTop|'''posTop''']], [[css/cssom/properties/posLeft|'''posLeft''']], [[css/cssom/properties/pixelHeight|'''pixelHeight''']], [[css/cssom/properties/pixelWidth|'''pixelWidth''']], [[css/cssom/properties/pixelTop|'''pixelTop''']], and [[css/cssom/properties/pixelLeft|'''pixelLeft''']].
To change or clear multiple style properties simultaneously, use this object with the [[css/cssom/styleSheet/cssText|'''cssText''']] property. For example, to change the font color and background color of a '''DIV''' element, you could use the following code:
 <code>
 &lt;DIV onclick{{=}}"this.style.cssText {{=}} 'color:red;background-color:blue;border:5px solid black;'"&gt;
 Click this DIV to change style properties.&lt;/DIV&gt;
 </code>
|Import_Notes====Standards information===
There are no standards that apply here.

===Members===
The '''style''' object has these types of members:
*[#methods Methods]
*[#properties Properties]

???? Test
====Methods==== 
The '''style''' object has these methods.
{| class="wikitable"
|-
!Method !! Description
|-
| [[dom/methods/getAttribute|'''getAttribute''']] || Retrieves the value of the specified attribute.
|-
| [[dom/methods/getAttributeNode|'''getAttributeNode''']] || Retrieves an [[dom/attributes|'''attribute''']] object referenced by the '''attribute''' [[html/attributes/name|'''name''']] property.
|-
| [[css/cssom/methods/getExpression|'''getExpression''']] || Retrieves the expression for the given property.
|-
| [[css/cssom/CSSStyleDeclaration/getPropertyPriority|'''getPropertyPriority''']] || Gets the priority of a CSS property if the priority  is  explicitly set in the current declaration block.
|-
| [[css/cssom/CSSStyleDeclaration/getPropertyValue|'''getPropertyValue''']] || Gets  the value of a CSS property if it is explicitly set within the current declaration block.
|-
| [[dom/methods/hasAttribute|'''hasAttribute''']] || Determines whether an attribute with the specified name exists.
|-
| [[dom/methods/hasAttributes|'''hasAttributes''']] || Determines whether one or more attributes exist for the object.
|-
| [[css/cssom/CSSStyleDeclaration/item|'''item''']] || Gets a property that has been explicitly set in the current declaration block.
|-
| [[css/cssom/methods/msGetPropertyEnabled|'''msGetPropertyEnabled''']] || Returns whether a given property in the style object is enabled.
|-
| [[css/cssom/methods/msPutPropertyEnabled|'''msPutPropertyEnabled''']] || Sets whether a given property in the style object is enabled.
|-
| [[dom/methods/normalize|'''normalize''']] || Merges adjacent DOM objects to produce a normalized document object model.
|-
| [[dom/methods/removeAttribute|'''removeAttribute''']] || Removes an attribute from an object.
|-
| [[dom/methods/removeAttributeNode|'''removeAttributeNode''']] || Removes an [[dom/attributes|'''attribute''']] object from the object.
|-
| [[css/cssom/methods/removeExpression|'''removeExpression''']] || Removes the expression from the specified property.
|-
| [[css/cssom/methods/removeProperty|'''removeProperty''']] || Removes a CSS property if it  is  explicitly set within the current declaration block.
|-
| [[dom/methods/setAttribute|'''setAttribute''']] || Sets the value of the specified attribute.
|-
| [[dom/methods/setAttributeNode|'''setAttributeNode''']] || Sets an [[dom/attributes|'''attribute''']] object node as part of the object.
|-
| [[css/cssom/methods/setExpression|'''setExpression''']] || Sets an expression for the specified object.
|-
| [[css/cssom/methods/setProperty|'''setProperty''']] || Sets a property value and priority within the current declaration block.
|}

====Properties====
The '''style''' object has these properties.
{| class="wikitable"
|-
!Property !! Description
|-
|[[css/media queries/accelerator|'''accelerator''']] || Sets or retrieves a string that indicates whether the object represents a keyboard shortcut.
|-
|[[css/properties/animation/animation|'''animation''']]
|Gets or sets one or more shorthand values  that specify all animation properties (except   [[css/properties/animation-play-state|'''animation-play-state''']]) for a set of corresponding object properties  identified in the CSS [[css/atrules/@keyframes|'''@keyframes''']] at-rule specified by the [[css/properties/animation-name|'''animation-name''']] property.
|-
|[[css/properties/animation-delay|'''animationDelay''']]
|Gets or sets one or more values  that specify the offset within an animation cycle (the amount of time from the start of a cycle) before  the animation  is displayed  for a set of corresponding object properties  identified in the CSS [[css/atrules/@keyframes|'''@keyframes''']] at-rule specified by the [[css/properties/animation-name|'''animation-name''']] property.
|-
|[[css/properties/animation-direction|'''animationDirection''']]
|Gets or sets one or more values  that specify the direction of play for an animation cycle.
|-
|[[css/properties/animation-duration|'''animationDuration''']]
|Gets or sets one or more values that specify the length of time to complete one cycle of the animation.
|-
|[[css/properties/animation-fill-mode|'''animationFillMode''']]
|Gets or sets one or more values  that specify whether the effects of an animation are visible before or after it plays.
|-
|[[css/properties/animation-iteration-count|'''animationIterationCount''']]
|Gets or sets one or more values  that specify the number of times an animation cycle is played.
|-
|[[css/properties/animation-name|'''animationName''']]
|Gets or sets a value  that identifies one or more animation names. An animation name identifies (or selects) a  CSS [[css/atrules/@keyframes|'''@keyframes''']] at-rule.
|-
|[[css/properties/animation-play-state|'''animationPlayState''']]
|Gets or sets one or more values  that specify whether an animation is playing or paused.
|-
|[[css/properties/animation-timing-function|'''animationTimingFunction''']]
|Gets or sets one or more values  that specify the intermediate property values to be used during a single cycle of an animation on a set of corresponding object properties  identified in the CSS [[css/atrules/@keyframes|'''@keyframes''']] at-rule specified by the [[css/properties/animation-name|'''animationName''']] property.
|-
|[[dom/properties/attributes|'''attributes''']]
|Retrieves a collection of attributes of the object.
|-
|[[css/properties/backface-visibility|'''backfaceVisibility''']]
|Gets or sets a value  that specifies whether the back face (reverse side) of an  object is visible.
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
|[[css/properties/background-clip|'''backgroundClip''']]
|Sets or retrieves the background painting area.
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
|[[css/properties/background-size|'''backgroundSize''']]
|Sets or retrieves the size of the background images.
|-
|[[svg/attributes/baseline-shift|'''baselineShift''']]
|Sets or retrieves a value that indicates how the dominant baseline should be repositioned relative to the dominant baseline of the parent text content element.
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
|[[css/properties/break-after|'''breakAfter''']]
|Gets or sets the column-break behavior that follows a content block in a multi-column element.
|-
|[[css/properties/break-before|'''breakBefore''']]
|Gets or sets the column-break behavior that precedes a content block in a multi-column element.
|-
|[[css/properties/break-inside|'''breakInside''']]
|Gets or sets the column-break behavior that occurs within a content block in a multi-column element.
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
|[[css/cssom/properties/clipBottom|'''clipBottom''']]
|Gets the bottom coordinate of the object clipping region.
|-
|[[css/cssom/properties/clipLeft|'''clipLeft''']]
|Gets the left coordinate of the object clipping region.
|-
|[[svg/properties/clipPath|'''clipPath''']]
|Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
|-
|[[css/cssom/properties/clipRight|'''clipRight''']]
|Gets the right coordinate of the object clipping region.
|-
|[[css/cssom/properties/clipTop|'''clipTop''']]
|Gets the top coordinate of the object clipping region.
|-
|[[css/properties/color|'''color''']]
|Sets or retrieves  the color of the text of the object.
|-
|[[css/properties/column-count|'''columnCount''']]
|Gets or sets the optimal number of columns in a multi-column element.
|-
|[[css/properties/column-fill|'''columnFill''']]
|Gets or sets a value that indicates how the column lengths in a multi-column element are affected by the content flow.
|-
|[[css/properties/column-gap|'''columnGap''']]
|Gets or sets the width of the gap between columns in a multi-column element.
|-
|[[css/properties/column-rule|'''columnRule''']]
|Gets or sets a shorthand value  that specifies values for the [[css/properties/column-rule-width|'''columnRuleWidth''']],  [[css/properties/column-rule-style|'''columnRuleStyle''']], and the [[css/properties/column-rule-color|'''columnRuleColor''']] of a multi-column element.
|-
|[[css/properties/column-rule-color|'''columnRuleColor''']]
|Gets or sets the color for all column rules in a multi-column element.
|-
|[[css/properties/column-rule-style|'''columnRuleStyle''']]
|Gets or sets the style for all column rules in a multi-column element.
|-
|[[css/properties/column-rule-width|'''columnRuleWidth''']]
|Gets or sets  the width of all column rules in a multi-column element.
|-
|[[css/properties/column-span|'''columnSpan''']]
|Gets or sets the number of columns that a content block spans in a multi-column element.
|-
|[[css/properties/column-width|'''columnWidth''']]
|Gets or sets the optimal width of the columns in a multi-column element.
|-
|[[dom/properties/constructor|'''constructor''']]
|Returns a reference to the constructor of an object.
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
|[[css/cssom/properties/cssFloat|'''cssFloat''']]
|Sets or retrieves a value that specifies whether a box should float to the left, right, or not at all.
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
|[[css/properties/display|'''display''']]
|Gets or sets a value that indicates  whether and how the object is rendered.
|-
|[[svg/attributes/dominant-baseline|'''dominantBaseline''']]
|Sets or retrieves a value that determines or redetermines a scaled-baseline table.
|-
|[[css/properties/empty-cells|'''emptyCells''']]
|Determines whether to show or hide a cell without content.
|-
|[[svg/attributes/fill|'''fill''']]
|Sets or retrieves a value that indicates the color to paint the interior of the given graphical element.
|-
|[[svg/attributes/fill-opacity|'''fillOpacity''']]
|Sets or retrieves a value that specifies the opacity of the painting operation that is used to paint the interior of the current object.
|-
|[[svg/attributes/fill-rule|'''fillRule''']]
|Sets or retrieves a value that indicates the algorithm that is to be used to determine what parts of the canvas are included inside the shape.
|-
|[[css/media queries/filter|'''filter''']]
|Sets or retrieves  the filter or collection of filters that are applied to the object.
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
|[[svg/attributes/glyph-orientation-horizontal|'''glyphOrientationHorizontal''']]
|Sets or retrieves a value that alters the orientation of a sequence of characters relative to an inline-progression-direction  of horizontal.
|-
|[[svg/attributes/glyph-orientation-vertical|'''glyphOrientationVertical''']]
|Sets or retrieves a value that alters the orientation of a sequence of characters relative to an inline-progression-direction of vertical.
|-
|[[css/properties/height|'''height''']]
|Sets or retrieves  the height of the object.
|-
|[[css/properties/ime-mode|'''imeMode''']]
|Sets or retrieves the state of an IME.
|-
|[[svg/attributes/kerning|'''kerning''']]
|Gets or sets a value that indicates whether Internet Explorer should adjust inter-glyph spacing based on kerning tables that are included in the relevant font (that is, enable auto-kerning) or instead disable auto-kerning and set inter-character spacing to a specific length (typically zero).

Gets or sets a value that indicates whether Metro style app using JavaScript should adjust inter-glyph spacing based on kerning tables that are included in the relevant font (that is, enable auto-kerning) or instead disable auto-kerning and set inter-character spacing to a specific length (typically zero).
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
|[[css/cssom/properties/length|'''length''']]
|Retrieves  the number of properties that  are  explicitly set on the parent object.
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
|[[svg/attributes/marker|'''marker''']]
|Sets or retrieves a value that specifies the marker symbol that is used for all vertices on the given [[svg/elements/path|'''path''']] element or basic shape.
|-
|[[svg/attributes/marker-end|'''markerEnd''']]
|Sets or retrieves a value that defines the arrowhead or polymarker that is drawn at the final vertex of a given [[svg/elements/path|'''path''']] element or basic shape.
|-
|[[svg/attributes/marker-mid|'''markerMid''']]
|Sets or retrieves a value that defines the arrowhead or polymarker that is drawn at every other vertex (that is, every vertex except the first and last) of a given [[svg/elements/path|'''path''']] element or basic shape.
|-
|[[svg/attributes/marker-start|'''markerStart''']]
|Sets or retrieves a value that defines the arrowhead or polymarker that is drawn at the first vertex of a given [[svg/elements/path|'''path''']] element or basic shape.
|-
|[[svg/attributes/mask|'''mask''']]
|Sets or retrieves a value that indicates a SVG mask.
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
|[[css/properties/ms-box-align|'''msBoxAlign''']]
|Do not use. This property has been replaced by the [[css/properties/ms-flex-align|'''-ms-flex-align''']] property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
|-
|[[css/properties/ms-box-direction|'''msBoxDirection''']]
|Do not use. This property has been replaced by the [[css/properties/ms-flex-direction|'''-ms-flex-direction''']] property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
|-
|[[css/properties/ms-box-flex|'''msBoxFlex''']]
|Do not use. This property has been replaced by the [[css/properties/ms-flex|'''-ms-flex''']] property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
|-
|[[css/properties/ms-box-line-progression|'''msBoxLineProgression''']]
|Do not use. This property has been replaced by the [[css/properties/ms-flex-wrap|'''-ms-flex-wrap''']] property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
|-
|[[css/properties/ms-box-lines|'''msBoxLines''']]
|Do not use. This property has been replaced by the [[css/properties/ms-flex-wrap|'''-ms-flex-wrap''']] property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
|-
|[[css/properties/ms-box-ordinal-group|'''msBoxOrdinalGroup''']]
|Do not use. This property has been replaced by the [[css/properties/ms-flex-order|'''-ms-flex-order''']] property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
|-
|[[css/properties/ms-box-orient|'''msBoxOrient''']]
|Do not use. This property has been replaced by the [[css/properties/ms-flex-direction|'''-ms-flex-direction''']] property, and is no longer recognized by Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly.
|-
|[[css/properties/ms-grid-column|'''msGridColumn''']]
|Gets or sets a value  that specifies in which column of the grid to place the object.
|-
|[[css/properties/ms-grid-column-align|'''msGridColumnAlign''']]
|Gets or sets a value  that specifies the horizontal alignment of the object within the  grid column.
|-
|[[css/properties/ms-grid-columns|'''msGridColumns''']]
|Gets or sets one or more values that specify the width of each grid column within the object.
|-
|[[css/properties/ms-grid-column-span|'''msGridColumnSpan''']]
|Gets or sets a value  that specifies the number of  columns of the grid that the object spans.
|-
|[[css/properties/ms-grid-row|'''msGridRow''']]
|Gets or sets a value  that specifies in which row of the grid to place the object.
|-
|[[css/properties/ms-grid-row-align|'''msGridRowAlign''']]
|Gets or sets a value  that specifies the vertical alignment of the object within the  grid row.
|-
|[[css/properties/ms-grid-rows|'''msGridRows''']]
|Gets or sets one or more values  that specify the height of each grid row within the object.
|-
|[[css/properties/ms-grid-row-span|'''msGridRowSpan''']]
|Gets or sets a value  that specifies the number of  rows of the grid that the object spans.
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
|[[css/cssom/CSSRule/parentRule|'''parentRule''']]
|Retrieves the containing rule, if the current rule is contained inside another rule.
|-
|[[css/properties/perspective|'''perspective''']]
|Gets or sets a value  that represents the perspective from which all child elements of the object are viewed.
|-
|[[css/properties/perspective-origin|'''perspectiveOrigin''']]
|Gets or sets one or two values  that represent the origin (the vanishing point for the 3-D space) of an object with an [[css/properties/perspective|'''perspective''']] property declaration.
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
|[[svg/attributes/pointers|'''pointerEvents''']]
|Sets or retrieves a value that specifies under what circumstances a given graphics element can be the target element for a pointer event in SVG.
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
|[[html/attributes/role|'''role''']]
|Sets or retrieves the role for this element.
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
|[[svg/attributes/stop-color|'''stopColor''']]
|Sets or retrieves a value that indicates what color to use at the current gradient stop.
|-
|[[svg/attributes/stop-opacity|'''stopOpacity''']]
|Sets or retrieves a value that defines the opacity of the current gradient stop.
|-
|[[svg/attributes/stroke|'''stroke''']]
|Sets or retrieves a value that indicates the color to paint along the outline of a given graphical element.
|-
|[[svg/attributes/stroke-dasharray|'''strokeDasharray''']]
|Sets or retrieves one or more values that indicate the pattern of dashes and gaps used to stroke paths.
|-
|[[svg/attributes/stroke-dashoffset|'''strokeDashoffset''']]
|Sets or retrieves a value that specifies the distance into the dash pattern to start the dash.
|-
|[[svg/attributes/stroke-linecap|'''strokeLinecap''']]
|Sets or retrieves a value that specifies the shape to be used at the end of open subpaths when they are stroked.
|-
|[[svg/attributes/stroke-linejoin|'''strokeLinejoin''']]
|Sets or retrieves a value that specifies the shape to be used at the corners of paths or basic shapes when they are stroked.
|-
|[[svg/attributes/stroke-miterlimit|'''strokeMiterlimit''']]
|Sets or retrieves a value that indicates the limit on the ratio of the length of miter joins (as specified in the [[svg/attributes/stroke-linejoin|'''strokeLinejoin''']] property).
|-
|[[svg/attributes/stroke-opacity|'''strokeOpacity''']]
|Sets or retrieves a value that specifies the opacity of the painting operation that is used to stroke the current object.
|-
|[[svg/attributes/stroke-width|'''strokeWidth''']]
|Sets or retrieves a value that specifies the width of the stroke on the current object.
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
|[[css/transforms/transform|'''transform''']]
|Gets or sets a list of one or more transform functions that specify how to translate, rotate, or scale an element in 2-D or 3-D space.
|-
|[[css/properties/transform-origin|'''transformOrigin''']]
|Gets or sets one or two values that establish the origin of transformation for an element.
|-
|[[css/properties/transform-style|'''transformStyle''']]
|Gets or sets a value  that specifies how child elements of the object are rendered in 3-D space.
|-
|[[css/properties/transition|'''transition''']]
|Gets or sets one or more shorthand values  that specify the transition properties  for a set of corresponding object properties  identified in the [[css/properties/transition-property|'''transition-property''']] property.
|-
|[[css/properties/transition-delay|'''transitionDelay''']]
|Gets or sets one or more values  that specify the offset within a transition (the amount of time from the start of a transition) before  the transition  is displayed  for a set of corresponding object properties  identified in the [[css/properties/transition-property|'''transition-property''']] property.
|-
|[[css/properties/transition-duration|'''transitionDuration''']]
|Gets or sets one or more values  that specify the durations of transitions on a set of corresponding object properties  identified in the [[css/properties/transition-property|'''transition-property''']] property.
|-
|[[css/properties/transition-property|'''transitionProperty''']]
|Gets or sets a value  that identifies the CSS property name or names to which the transition effect (defined by [[css/properties/transition-duration|'''transition-duration''']], [[css/functions/transition-timing-function|'''transition-timing-function''']], and [[css/properties/transition-delay|'''transition-delay''']]) is applied when a new property value is specified.
|-
|[[css/functions/transition-timing-function|'''transitionTimingFunction''']]
|Gets or sets one or more values  that specify the intermediate property values to be used during a transition on a set of corresponding object properties  identified in the [[css/properties/transition-property|'''transition-property''']] property.
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
|[[css/properties/white-space|'''whiteSpace''']]
|Sets or retrieves a value that indicates whether lines are automatically broken inside the object.
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
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Style Attributes
|URL=http://www.w3.org/TR/css-style-attr/
|Status=Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=CSSOM
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}