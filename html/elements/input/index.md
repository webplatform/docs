{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Element
|DOM_interface=dom/HTMLInputElement
}}
{{Topics|HTML}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''input''' element to create different types of input controls.
|LiveURL=
|Code=
&lt;form action{{=}}"http://intranet/survey" method{{=}}post&gt;
&lt;p&gt;Name&lt;/p&gt;
&lt;br&gt;&lt;input name{{=}}"control1" type{{=}}text value{{=}}"Your Name"&gt;
&lt;P&gt;Password&lt;/P&gt;
&lt;br&gt;&lt;input type{{=}}"password" name{{=}}"control2"&gt;
&lt;p&gt;Color&lt;/p&gt;
&lt;br&gt;&lt;input type{{=}}"radio" name{{=}}"control3" value{{=}}"0" checked&gt;Red
&lt;input type{{=}}"radio" name{{=}}"control3" value{{=}}"1"&gt;Green
&lt;input type{{=}}"radio" name{{=}}"control3" value{{=}}"2"&gt;Blue
&lt;p&gt;Comments&lt;/p&gt;
&lt;br&gt;&lt;input type{{=}}"TEXT" name{{=}}"control4" size{{=}}"20,5" maxlength{{=}}"250"&gt;
&lt;p&gt;&lt;input name{{=}}"control5" type{{=}}checkbox checked&gt;Send receipt&lt;/p&gt;
&lt;p&gt;&lt;input type{{=}}"submit" value{{=}}"OK"&gt;&lt;input type{{=}}"reset" value{{=}}"reset"&gt;&lt;/p&gt;
&lt;/form&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
In IE8 Standards mode, the [[html/attributes/title|'''title''']] attribute is preferred over the [[html/attributes/alt|'''alt''']] attribute when specified as a pop-up tooltip. This applies only when the [[html/attributes/type|'''type''']] attribute is set to <code>image</code>. For more info, see Defining Document Compatibility.
'''Note'''  For code samples, see [http://go.microsoft.com/fwlink/p/?LinkID{{=}}251128 Form controls part 1] and [http://go.microsoft.com/fwlink/p/?LinkID{{=}}251131 Form controls part 2: validation] on the Windows Internet Explorer sample site.
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML]
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5


===HTML information===
{| class="wikitable"
|-
!Closing Tag
|required
|-
!CSS Display
|inline
|-
!HTML Element Categories
|flow phrasing interactive
|}

===Members===
The '''HTMLInputElement''' object has these types of members:
*[#properties Properties]


====Properties====
The '''HTMLInputElement''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[html/attributes/accept|'''accept''']]
|Sets or retrieves a comma-separated list of content types.
|-
|[[html/attributes/align (type/image)|'''align''']]
|Sets or retrieves how the object is aligned with adjacent text.
|-
|[[html/attributes/alt|'''alt''']]
|Sets or retrieves a text alternative to the graphic.
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
|[[css/properties/backface-visibility|'''backfaceVisibility''']]
|Gets or sets a value  that specifies whether the back face (reverse side) of an  object is visible.
|-
|[[html/attributes/checked|'''checked''']]
|Sets or retrieves the state of the check box or radio button.
|-
|[[dom/properties/complete|'''complete''']]
|Retrieves whether the object is fully loaded.
|-
|[[dom/properties/constructor|'''constructor''']]
|Returns a reference to the constructor of an object.
|-
|'''dynsrc'''
|This property is deprecated. Sets or retrieves the address of a video clip or VRML world to display in the window.
|-
|[[html/attributes/hspace|'''hspace''']]
|Sets or retrieves the horizontal margin for the object.
|-
|[[html/attributes/loop|'''loop''']]
|Sets or retrieves the number of times a sound or video clip will loop when activated.
|-
|[[html/attributes/lowsrc|'''lowsrc''']]
|Sets or retrieves a lower resolution image to display.
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
|[[css/properties/perspective|'''perspective''']]
|Gets or sets a value  that represents the perspective from which all child elements of the object are viewed.
|-
|[[css/properties/perspective-origin|'''perspectiveOrigin''']]
|Gets or sets one or two values  that represent the origin (the vanishing point for the 3-D space) of an object with an [[css/properties/perspective|'''perspective''']] property declaration.
|-
|[[html/attributes/start|'''start''']]
|Sets or retrieves when a video clip file should begin playing.
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
|[[html/attributes/useMap|'''useMap''']]
|Sets or retrieves the URL, often with a bookmark extension (#name), to use as a client-side image map.
|-
|[[html/attributes/value (input elements)|'''value''']]
|Sets or retrieves the displayed value for the control object.  This value is returned to the server when the control object is submitted.
|-
|[[html/attributes/vspace|'''vspace''']]
|Sets or retrieves the vertical margin for the object.
|}
 

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>Reference</code>
*<code>button</code>
*<code>select</code>
*<code>textArea</code>
|Topic_clusters=html, form
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}