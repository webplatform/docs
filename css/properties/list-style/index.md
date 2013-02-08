{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Sets  list-style-type, list-style-position, list-style-image properties in one declaration.}}
{{CSS Property
|Initial value=disc outside none
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=type
|Description=Any of the range of type values available to the [[css/properties/list-style-type|'''list-style-type''']] property.
}}{{CSS Property Value
|Data Type=position
|Description=Any of the range of position values available to the [[css/properties/list-style-position|'''list-style-position''']] property.
}}{{CSS Property Value
|Data Type=image
|Description=Any of the range of image values available to the [[css/properties/list-style-image|'''list-style-image''']] property.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following examples use the list-style attribute and the '''list-style''' property to set the list style.

This example uses '''ul''' and <code>UL.compact</code> as selectors in an embedded (global) style sheet to define the styles of two different unordered lists.  For <code>UL.compact</code> to override the image that is set with the '''ul''' selector, you must explicitly set the '''image''' attribute to '''none'''.
|Code=ul { list-style: circle outside url('/workshop/graphics/dot.gif') }
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/list-style.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''list-style''' property is a composite property. When specifying both the '''type''' and '''image''' values, the '''image''' value takes precedence, unless the '''image''' value is set to '''none''' or the image pointed to by the URL cannot display.
The '''list-style''' property also applies to all elements on which the [[css/properties/display|'''display''']] property is set to '''list-item'''.  To make the bullet points appear, you must explicitly set the [[css/properties/margin|'''margin''']] property or set the [[css/properties/list-style-position|'''list-style-position''']] property to '''inside''' on these elements.
|Import_Notes====Syntax===
<code>'''list-style: ''''''[''' type '''{{!}}{{!}}''' position '''{{!}}{{!}}''' image ''']'''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.6.6
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
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=4.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=7.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
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
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Generated and Replaced Content
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}