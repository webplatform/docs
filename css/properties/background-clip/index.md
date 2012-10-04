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
|Values={{CSS_Property_Value|Data Type=border-box |Description=Default. The background is painted within (clipped to) the border box.}}
{{CSS_Property_Value|Data Type=padding-box |Description=The background is painted within (clipped to) the padding box.}}
{{CSS_Property_Value|Data Type=content-box |Description=The background is painted within (clipped to) the content box.}}
}}
{{Topics|CSS}}
{{Notes_Section
|Notes=
===Remarks===
In Windows Internet Explorer 9, the background of a box can have multiple layers. The number of layers is determined by the number of comma-separated values in the [[css/properties/background-image|'''background-image''']] property. Each of the images is sized, positioned, and tiled according to the corresponding value in the other background properties ([[css/properties/background-attachment|'''background-attachment''']], '''background-clip''', [[css/properties/background-origin|'''background-origin''']], [[css/properties/background-position|'''background-position''']], [[css/properties/background-repeat|'''background-repeat''']], and [[css/properties/background-size|'''background-size''']]). The first image in the list is the layer closest to the user, the next one is painted behind the first, and so on.
|Import_Notes=
===Syntax===
<code>'''background-clip: '''border-box '''{{!}}''' padding-box '''{{!}}''' content-box</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}197157 CSS Backgrounds and Borders Module Level 3], Section 3.7


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/style|style]]</code>
*<code>style</code>
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
*<code>[[css/properties/background-origin|background-origin]]</code>
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