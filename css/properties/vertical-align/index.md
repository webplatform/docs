{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>vertical-align</code> property controls how inline elements or text are vertically aligned compared to the baseline. If this property is used on table-cells it controls the vertical alignment of content of the table cell.}}
{{CSS Property
|Initial value=baseline
|Applies to=inline-level and ‘table-cell’ elements
|Inherited=No
|Media=visual
|Animatable=No
|CSS percentages=refers to the ‘line-height’ of the element itself
|Values={{CSS Property Value
|Data Type=baseline
|Description=Default. Vertically aligns the content with the baseline of its parent.
}}{{CSS Property Value
|Data Type=middle
|Description=Vertically aligns the content to the middle of its parent.
}}{{CSS Property Value
|Data Type=sub
|Description=Vertically aligns the content to subscript.
}}{{CSS Property Value
|Data Type=super
|Description=Vertically aligns the content to superscript.
}}{{CSS Property Value
|Data Type=text-top
|Description=Vertically aligns the content to the top of its parent.
}}{{CSS Property Value
|Data Type=text-bottom
|Description=Vertically aligns the content to the bottom of its parent.
}}{{CSS Property Value
|Data Type=&lt;percentage>
|Description=Raises or lowers the content by a percentage of the line height. If this is set to a positive number the content is raised compared to the baseline of its parent. If this is set to a negative number the content is lowered compared to the baseline of its parent. If set to <code>0</code> it is equivalent to <code>baseline</code>.
}}{{CSS Property Value
|Data Type=&lt;length>
|Description=Raises or lowers the content by the specified length. If this is set to a positive number the content is raised compared to the baseline of its parent. If this is set to a negative number the content is lowered compared to the baseline of its parent. If set to <code>0</code> it is equivalent to <code>baseline</code>.
}}{{CSS Property Value
|Data Type=top
|Description=Vertically aligns the content and its descendants to the top of the text line.
}}{{CSS Property Value
|Data Type=bottom
|Description=Vertically aligns the content and its descendants to the bottom of the text line.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the <code>vertical-align</code> property to align text within a table cell.
|Code=&lt;table>
  &lt;tr>
    &lt;td style='vertical-align: top;'>Top aligned&lt;/td>
    &lt;td style='vertical-align: middle;'>Middle aligned&lt;/td>
    &lt;td style='vertical-align: bottom;'>Bottom aligned&lt;/td>
  &lt;/tr>
&lt;/table>
|LiveURL=http://code.webplatform.org/gist/6960125
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Level 2 (Revision 1)
|URL=http://www.w3.org/TR/CSS2/visudet.html#propdef-vertical-align
|Status=Recommendation
}}
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
|Opera_version=4.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}