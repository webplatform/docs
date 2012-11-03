{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
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
|Description=Default. Column width is set by the widest unbreakable content in the column cells.
}}{{CSS Property Value
|Data Type=fixed
|Description=Table and column widths are set either by the sum of the widths on the '''col''' objects or, if these are not specified, by the width of the first row of cells. If no width is specified for the table, it renders by default with width{{=}}100%.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the CSS attribute to set the table layout to '''fixed'''.
|Code=&lt;TABLE STYLE{{=}}"table-layout:fixed" WIDTH{{=}}600&gt;
&lt;COL WIDTH{{=}}100&gt;&lt;COL WIDTH{{=}}300&gt;&lt;COL WIDTH{{=}}200&gt;
&lt;TR HEIGHT{{=}}20&gt;
&lt;TD&gt;...&lt;/TD&gt;&lt;TD&gt;...&lt;/TD&gt;&lt;TD&gt;...&lt;/TD&gt;
&lt;/TR&gt;
:
&lt;/TABLE&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
You can optimize table rendering performance by specifying the '''table-layout''' property. This property causes the table to be rendered one row at a time, providing users with information at a faster pace. The '''table-layout''' property determines column widths for a table in the following order:
#By using information in the [[html/attributes/width  (img, input elements)|'''width''']] property for the '''col''' or '''colGroup''' element.
#By using information in the [[html/attributes/width  (img, input elements)|'''width''']] property for the '''td''' elements in the first row.
#By dividing the table columns equally, regardless of the size of the content.

If the content of a cell exceeds the fixed width of the column, the content is wrapped or, if wrapping is not possible, it is clipped. If the '''table-layout''' property is set to '''fixed''', the [[css/properties/overflow|'''overflow''']] property can be used to handle content that exceeds the width of a '''td''' element. If the row height is specified, wrapped text is clipped when it exceeds the set height.
Setting the property to '''fixed''' significantly improves table rendering speed, particularly for longer tables.
Setting row height further improves rendering speed, again enabling the parser to begin rendering the row without examining the content of each cell in the row to determine row height.
|Import_Notes====Syntax===
<code>'''table-layout: '''auto '''{{!}}''' fixed</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 17.5.2
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=22.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=15.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=8.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
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
|Opera_mobile_supported=Yes
|Opera_mobile_version=2.1
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=IE
|Version=7
|Note="inherit" value is ignored for IE7 and earlier.
}}{{Compatibility Notes Row
|Browser=IE
|Version=8
|Note=HTML5  !DOCTYPE
}}
}}
{{See_Also_Section
|Topic_clusters=Tables
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[html/attributes/width  (img, input elements)|width]]</code>
*<code>Conceptual</code>
*<code>Enhancing Table Presentation</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}