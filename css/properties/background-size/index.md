{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Initial value=auto
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=for <length> the absolute value, otherwise a percentage
|Animatable=Yes
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
|Examples={{Single Example
|Language=CSS
|Code=/* Keywords syntax */
background-size: cover
background-size: contain

/* One-value syntax: the value defines the width of the image, the height is implicitly set to 'auto' */
background-size: 50%
background-size: 3em
background-size: 12px
background-size: auto

/* Two-value syntax: the first value defines the width fo the image, the second its height */
background-size: 50% auto
background-size: 3em 25%
background-size: auto 6px
background-size: auto auto

/* Values for the multiple backgrounds, defined by background-image, may be listed separated by commas */
background-size: auto, auto     /* Do not confuse this with background-size: auto auto */
background-size: 50%, 25%, 25%
background-size: 6px, auto, contain

background-size: inherit
}}
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
|Specifications={{Related Specification}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Basic support
|Chrome_supported=Yes
|Chrome_version=3+
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=1+
|Firefox_supported=Yes
|Firefox_version=4+
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=3.6
|Internet_explorer_supported=Yes
|Internet_explorer_version=9+
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10+
|Opera_prefixed_supported=Yes
|Opera_prefixed_version=9.5+
|Safari_supported=Yes
|Safari_version=4.1+
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=3.0+
}}{{Compatibility Table Desktop Row
|Feature=Support for contain and cover
|Chrome_supported=Yes
|Chrome_version=3+
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.6
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9+
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10+
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=4.1+
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=Support for SVG backgrounds
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=8+
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=Basic support
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Yes
|Android_prefixed_version=2.3+
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=Support for SVG backgrounds
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=8+
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Opera
|Version=9.5
|Note=Computation of the background positioning area is incorrect for fixed backgrounds. This version also interprets the two-value form as a horizontal scaling factor and, from appearances, a vertical clipping dimension.
}}{{Compatibility Notes Row}}
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
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/background-size
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}