{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Specifies the size of text. Sets the font size of the element to which it is applied, and its descendants. Can size text using absolute measurements, or relative to the parent or root elements. [[guides/css_text_styling_fundamentals|CSS Text Styling Fundamentals]] provides an overview.}}
{{CSS Property
|Initial value=medium
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=absolute size in px units
|Animatable=Yes
|CSS object model property=fontSize
|CSS percentages=???
|Values={{CSS Property Value
|Data Type=absolute-size
|Description=A set of keywords indicating predefined font sizes that scale according to font setting preferences or each browser's default values. From small to large, possible values are '''xx-small''', '''x-small''', '''small''', '''medium''', '''large''', '''x-large''', and '''xx-large'''.
}}{{CSS Property Value
|Data Type=relative-size
|Description=A set of keywords interpreted relative to the parent element's '''font-size''', either '''smaller''' or '''larger'''.
}}{{CSS Property Value
|Data Type=length
|Description=A positive numeric value followed by a string designating absolute units ([[css/units/cm|'''cm''']], [[css/units/mm|'''mm''']], [[css/units/in|'''in''']], [[css/units/pt|'''pt''']], [[css/units/pc|'''pc''']]) or relative units ([[css/units/px|'''px''']], [[css/units/rem|'''rem''']], [[css/units/em|'''em''']], [[css/units/ex|'''ex''']], [[css/units/vw|'''vw''']], [[css/units/vh|'''vh''']], [[css/units/vmin|'''vmin''']]). Proportional [[css/units/em|'''em''']] and [[css/units/ex|'''ex''']] measurements are based on the parent element's '''font-size''', while [[css/units/rem|'''rem''']] measurements are based on that of the root element.
}}{{CSS Property Value
|Data Type=percentage
|Description=A positive integer followed by a percent ([[css/units/percent|'''%''']]), indicating the proportion of the parent element's font-size.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Redefine the typical 16px default '''medium''' value as '''10px''', then redefine other tags in proportion to the root:
|Code=html { font-size: 62.5%; } /* 16 * 62.5% == 10 */

h1 { font-size: 3.6rem }   /* 36px */
h2 { font-size: 2.4rem }   /* 24px */
p  { font-size: 1.4rem }   /* 14px */

}}{{Single Example
|Language=HTML
|Description=This interactive utility demonstrates absolute values applied to a block of text, and relative values applied to the first sentence:
|LiveURL=http://letmespellitoutforyou.com/x/webplatform/fontSize.html
}}
}}
{{Notes_Section
|Usage=Keywords such as '''large''' and '''medium''', or relative '''em''' or percentage units, are generally safer to use than pixel measurements, especially for mobile web browsers that adjust their set of default font sizes for legibility. Otherwise, pixels offer the safest way to specify measurements, since [[css/concepts/CSS_pixels|CSS pixels]] are adjusted for variations in display pixel density.

While the initial '''medium''' size applies widely, browsers apply a default style sheet that modifies it for various semantic elements, boosting the size of headings, for example. Browsers also automatically resize fonts when zooming the page, stepping by values that may not correspond exactly to the zoom factor. Unless disabled using [[css/properties/text-size-adjust|'''text-size-adjust''']], fonts also resize when tipping between portrait and landscape orientations on mobile browsers. For an overview of the issue, see [[tutorials/mobile_viewport|The Mobile Viewport and Orientation]].

The value of '''font-size''' also affects the value of [[css/properties/line-height|'''line-height''']] when using its default or relative measurements.

Along with many other CSS properties, '''font-size''' can also be applied directly as an SVG attribute:

<syntaxhighlight lang="xml">
<text x="12px" y="12px" font-family="sans-serif" font-size="120%"/>
</syntaxhighlight>
|Notes====Remarks===
Negative values are not allowed. Font sizes using the proportional "em" measure are based on the font size of the parent object.
As of Microsoft Internet Explorer 6, when you use the [[html/elements/!DOCTYPE|!DOCTYPE]] declaration to specify standards-compliant mode, the default value for this property is <code>medium</code>, not <code>small</code>.
Possible length values specified in a relative measurement, using the height of the element's font (em) or the height of the letter "x" (ex), are supported in Microsoft Internet Explorer 4.0 and later.
|Import_Notes====Syntax===
<code>'''font-size: '''''
&lt;absolute-size&gt;
'' '''{{!}}''' ''
&lt;relative-size&gt;
'' '''{{!}}''' ''
&lt;length&gt;
'' '''{{!}}''' ''
&lt;percentage&gt;
''</code>
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=5.5
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=7.0
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=1.0
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=3.8
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=1.0
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1.0
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=6.0
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=6.0
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=1.0
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=1.0
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSS Font, Fonts, Text
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/font|font]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}