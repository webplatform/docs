{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=auto
|Description=Default. See Remarks.
}}{{CSS Property Value
|Data Type=contain
|Description=Scale the image, while preserving its intrinsic aspect ratio (if any), to the largest size such that both its width and its height can fit inside the background positioning area.
}}{{CSS Property Value
|Data Type=cover
|Description=Scale the image, while preserving its intrinsic aspect ratio (if any), to the smallest size such that both its width and its height can completely cover the background positioning area.
}}{{CSS Property Value
|Data Type=length
|Description=A floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). 
For more information about the supported length units, see the CSS Values and Units Reference.
}}{{CSS Property Value
|Data Type=percentage
|Description=An integer, followed by a percent (%). A percentage value is relative to the background positioning area.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
An <code>auto</code> value for one dimension is resolved by using the image's intrinsic ratio and the size of the other dimension. If either of these values is not available, the image's intrinsic size is used. If the image's intrinsic size is not available, it is assigned the value of 100%. If both values are <code>auto</code>, use the intrinsic width, height, or both, of the image. If the image has neither an intrinsic width nor an intrinsic height, its size is determined as for <code>contain</code>.
Negative values are not allowed.
In Windows Internet Explorer 9, the background of a box can have multiple layers. The number of layers is determined by the number of comma-separated values in the [[css/properties/background-image|'''background-image''']] property. Each of the images is sized, positioned, and tiled according to the corresponding value in the other background properties ([[css/properties/background-attachment|'''background-attachment''']], [[css/properties/background-clip|'''background-clip''']], [[css/properties/background-origin|'''background-origin''']], [[css/properties/background-position|'''background-position''']], [[css/properties/background-repeat|'''background-repeat''']], and '''background-size'''). The first image in the list is the layer closest to the user, the next one is painted behind the first, and so on.
|Import_Notes====Syntax===
<code>'''background-size: '''auto '''{{!}}''' contain '''{{!}}''' cover '''{{!}}''' ''
&lt;percentage&gt;
'' '''{{!}}''' ''
&lt;length&gt;
''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}197157 CSS Backgrounds and Borders Module Level 3], Section 3.9
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Full Suport
|Chrome_supported=Yes
|Chrome_version=22+
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=15+
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12+
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Background
|Manual_sections====Related pages (MSDN)===
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
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}