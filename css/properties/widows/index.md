{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
|Editorial notes=The "widows" CSS property helps to set or return the minimum number of lines for an element(for eg: paragraph) that must be visible at the top of a page. It affects on the block level elements. 
It can have a number value or it can inherit the values from the parent element.
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Initial value=2
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=integer
|Description=A '''VARIANT''' that specifies or receives
the minimum number of lines to print at the top of a document.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following style rule ensures that at least three lines
of a paragraph appear at the bottom and top of each printed document.
|Code=&lt;meta http-equiv{{=}}"X-UA-Compatible" content{{=}}"IE{{=}}8" /&gt;
&lt;style type{{=}}"text/css"&gt;
@media print {
    p {
        widows:3;
        orphans:3;
    }
}
&lt;/style&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
This property applies when the document is printed.
If there are fewer lines than necessary to satisfy this rule,
the lines are moved to the following document. The
'''widows'''
property has precedence over the
[[css/properties/orphans|'''orphans''']] property.
This property requires Windows Internet Explorer to be in
IE8 Standards mode rendering.
|Import_Notes====Syntax===
<code>'''widows: '''integer</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 13.3
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=8.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Yes
|Opera_prefixed_version=9.2
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Paged Media
|External_links=http://www.w3schools.com/jsref/prop_style_widows.asp
http://xhtml.com/en/css/reference/widows/
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/orphans|orphans]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}