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
|Values={{CSS_Property_Value|Data Type=auto |Description=Default. See Remarks.}}
{{CSS_Property_Value|Data Type=contain |Description=Scale the image, while preserving its intrinsic aspect ratio (if any), to the largest size such that both its width and its height can fit inside the background positioning area.}}
{{CSS_Property_Value|Data Type=cover |Description=Scale the image, while preserving its intrinsic aspect ratio (if any), to the smallest size such that both its width and its height can completely cover the background positioning area.}}
{{CSS_Property_Value|Data Type=length |Description=A floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). 
For more information about the supported length units, see the CSS Values and Units Reference.}}
{{CSS_Property_Value|Data Type=percentage |Description=An integer, followed by a percent (%). A percentage value is relative to the background positioning area.}}
}}
{{Topics|CSS}}
{{Notes_Section
|Notes=
===Remarks===
An <code>auto</code> value for one dimension is resolved by using the image's intrinsic ratio and the size of the other dimension. If either of these values is not available, the image's intrinsic size is used. If the image's intrinsic size is not available, it is assigned the value of 100%. If both values are <code>auto</code>, use the intrinsic width, height, or both, of the image. If the image has neither an intrinsic width nor an intrinsic height, its size is determined as for <code>contain</code>.
Negative values are not allowed.
In Windows Internet Explorer 9, the background of a box can have multiple layers. The number of layers is determined by the number of comma-separated values in the [[css/properties/background-image|'''background-image''']] property. Each of the images is sized, positioned, and tiled according to the corresponding value in the other background properties ([[css/properties/background-attachment|'''background-attachment''']], [[css/properties/background-clip|'''background-clip''']], [[css/properties/background-origin|'''background-origin''']], [[css/properties/background-position|'''background-position''']], [[css/properties/background-repeat|'''background-repeat''']], and '''background-size'''). The first image in the list is the layer closest to the user, the next one is painted behind the first, and so on.
|Import_Notes=
===Syntax===
<code>'''background-size: '''auto '''{{!}}''' contain '''{{!}}''' cover '''{{!}}''' ''
&lt;percentage&gt;
'' '''{{!}}''' ''
&lt;length&gt;
''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}197157 CSS Backgrounds and Borders Module Level 3], Section 3.9


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>LayoutRect</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>style</code>
*<code>Reference</code>
*<code>[[css/properties/background-color|background-color]]</code>
*<code>[[css/properties/background-image|background-image]]</code>
*<code>[[css/properties/background-repeat|background-repeat]]</code>
*<code>[[css/properties/background-attachment|background-attachment]]</code>
*<code>[[css/properties/background-position|background-position]]</code>
*<code>[[css/properties/background-clip|background-clip]]</code>
*<code>[[css/properties/background-origin|background-origin]]</code>
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