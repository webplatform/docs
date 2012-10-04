{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=All elements
|Media=visual
|Inherited=No
|Initial value=
|Values={{CSS_Property_Value|Data Type=padding-box |Description=Default. The position is relative to the padding box. For single boxes, "0 0" is the upper-left corner of the padding edge; "100% 100%" is the lower-right corner.}}
{{CSS_Property_Value|Data Type=border-box |Description=The position is relative to the border box.}}
{{CSS_Property_Value|Data Type=content-box |Description=The position is relative to the content box.}}
}}
{{Topics|CSS}}
{{Notes_Section
|Notes=
===Remarks===
For elements rendered as a single box, the '''background-origin''' property specifies the background positioning area. For elements rendered as multiple boxes (for instance, inline boxes on several lines or boxes on several pages), this property specifies which boxes determine the background positioning areas.
If the [[css/properties/background-attachment|'''background-attachment''']] value for this image is '''fixed''', then the '''background-origin''' property has no effect. In this case, the background positioning area is the initial containing block.
In Windows Internet Explorer 9, the background of a box can have multiple layers. The number of layers is determined by the number of comma-separated values in the [[css/properties/background-image|'''background-image''']] property. Each of the images is sized, positioned, and tiled according to the corresponding value in the other background properties ([[css/properties/background-attachment|'''background-attachment''']], [[css/properties/background-clip|'''background-clip''']], '''background-origin''', [[css/properties/background-position|'''background-position''']], [[css/properties/background-repeat|'''background-repeat''']], and [[css/properties/background-size|'''background-size''']]). The first image in the list is the layer closest to the user, the next one is painted behind the first, and so on.
|Import_Notes=
===Syntax===
<code>'''background-origin: '''padding-box '''{{!}}''' border-box '''{{!}}''' content-box</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}197157 CSS Backgrounds and Borders Module Level 3], Section 3.8


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>LayoutRect</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>style</code>
*<code>Reference</code>
*<code>[[css/properties/background-color|background-color]]</code>
*<code>[[css/properties/background-image|background-image]]</code>
*<code>[[css/properties/background-repeat|background-repeat]]</code>
*<code>[[css/properties/background-attachment|background-attachment]]</code>
*<code>[[css/properties/background-position|background-position]]</code>
*<code>[[css/properties/background-clip|background-clip]]</code>
*<code>[[css/properties/background-size|background-size]]</code>
*<code>[[css/cssom/properties/background|background]]</code>
|Topic_clusters=Background
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}