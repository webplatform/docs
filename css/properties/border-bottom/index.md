{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Shorthand property that sets the properties of an element's bottom border.It can be used to set one or more values (of those: [[css/properties/border-bottom-width|'''border-bottom-width''']], [[css/properties/border-bottom-style|'''border-bottom-style''']], [[css/properties/border-bottom-color|'''border-bottom-color''']]).}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=See individual properties
|Animatable=No
|CSS object model property=borderBottom
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=<border-width> <border-style> <color>
|Description=The <tt>border-bottom</tt> property is a shorthand property for setting the same width, color, and style for only one border of a box: bottom.
* '''Width''' - Any of the range of width values available to the [[css/properties/border-bottom-width|'''border-bottom-width''']] property. It's optional. Default value is <tt>medium</tt>.
* '''Style''' - Any of the range of style values available to the [[css/properties/border-bottom-style|'''border-bottom-style''']] property. Default value is <tt>none</tt>.
* '''Color''' - Any of the range of color values available to the [[css/properties/border-bottom-color|'''border-bottom-color''']] property. Default value is the value of the element's [[css/properties/color|'''color''']] property - i.e. text color.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''border-bottom''' property and the '''border-bottom''' attribute to specify the various properties for the bottom border.

This example uses a call to an embedded (global) style sheet to change the attributes of the bottom border.
|Code=&lt;HEAD&gt;
&lt;STYLE&gt;
    TD 	{ border-bottom:0.5cm solid yellow }
    .change { border-bottom:0.5cm groove pink }
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;TABLE&gt;
&lt;TR&gt;
&lt;TD onmouseover{{=}}"this.className{{=}}'change'"
    onmouseout{{=}}"this.className{{=}}''"&gt;&lt;IMG src{{=}}"sphere.jpg"&gt;&lt;/TD&gt;
&lt;/TR&gt;
&lt;/TABLE&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/border-bottom.htm
}}{{Single Example
|Description=This example uses inline scripting to change the bottom border.
|Code=&lt;TD onmouseover{{=}}"this.style.borderBottom{{=}}'0.3cm groove yellow'"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/borderBottom.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''border-bottom''' property is a composite property that sets the '''width''', '''style''', and '''color''' values for the bottom border of an object.
All individual border properties not set by the composite '''border-bottom''' property are set to their default values. For example, the default value for '''width''' is '''medium'''.
If a '''color''' is not specified, the text color is used.
For more information about supported colors, see the Color Table.
As of Microsoft Internet Explorer 5.5, this property applies to inline elements.  With earlier versions of  Windows Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.5.20
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
|Firefox_version=1.0 ( 1.7 or earlier )
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=4
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=3.5
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
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1.0 (1.0)
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Border
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/properties/border|border]]</code>
*<code>Other Resources</code>
*<code>CSS Enhancements in Internet Explorer 6</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms530724(v=vs.85).aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}