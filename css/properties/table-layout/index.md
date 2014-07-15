{{Page_Title|table layout}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The 'table-layout' property controls the algorithm used to lay out the table cells, rows, and columns.}}
{{CSS Property
|Initial value=auto
|Applies to=Table and inline-table elements
|Inherited=No
|Media=visual
|Computed value=As specified
|Animatable=No
|CSS object model property=object.style.tableLayout
|Values={{CSS Property Value
|Data Type=auto
|Description=Default. Column width is set by the widest unbreakable content in the column cells. The width of the table and its cells depends on the content of the cells.
}}{{CSS Property Value
|Data Type=fixed
|Description=Table and column widths are set by the widths of table and col elements or by the width of the first row of cells. It does not depend on the content of the cells. Rendering is faster as the user agent can begin to lay out the table once the entire first row has been received. Cells in subsequent rows do not affect column widths.
}}{{CSS Property Value
|Data Type=inherit
|Description=This features inherits table-layout property  from the parent element.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example shows table-layout 'auto' and 'fixed'. With 'auto', the column stretches to encompass the largest unbreakable element. With 'fixed', the column gets the defined width, even though the content might not fit.
|Code=&lt;p&gt;&lt;strong&gt;table-layout: auto&lt;/strong&gt;&lt;/p&gt;
&lt;table border=&quot;1&quot;&gt;
	&lt;tr&gt;
		&lt;td class=&quot;first&quot;&gt;&lt;p&gt;cell 1, Lorem ipsum&lt;/p&gt;&lt;/td&gt;
		&lt;td&gt;&lt;p&gt;cell 2&lt;/p&gt;&lt;/td&gt;
	&lt;/tr&gt;
	&lt;tr&gt;
		&lt;td&gt;&lt;p&gt;cell 3, Suspendisse in elit lectus.&lt;/p&gt;&lt;/td&gt;
		&lt;td&gt;&lt;p&gt;cell 4&lt;/p&gt;&lt;/td&gt;
	&lt;/tr&gt;
&lt;/table&gt;

&lt;p&gt;&lt;strong&gt;table-layout: fixed&lt;/strong&gt;&lt;/p&gt;
&lt;table border=&quot;1&quot; class=&quot;fixed&quot;&gt;
	&lt;tr&gt;
		&lt;td class=&quot;first&quot;&gt;&lt;p&gt;cell 1, Lorem ipsum&lt;/p&gt;&lt;/td&gt;
		&lt;td&gt;&lt;p&gt;cell 2&lt;/p&gt;&lt;/td&gt;
	&lt;/tr&gt;
	&lt;tr&gt;
		&lt;td&gt;&lt;p&gt;cell 3, Suspendisse in elit lectus.&lt;/p&gt;&lt;/td&gt;
		&lt;td&gt;&lt;p&gt;cell 4&lt;/p&gt;&lt;/td&gt;
	&lt;/tr&gt;
&lt;/table&gt;

&lt;p&gt;&lt;strong&gt;table-layout: fixed with overflow set to hidden&lt;/strong&gt;&lt;/p&gt;
&lt;table border=&quot;1&quot; class=&quot;fixed2&quot;&gt;
	&lt;tr&gt;
		&lt;td class=&quot;first&quot;&gt;&lt;p&gt;cell 1, Lorem ipsum&lt;/p&gt;&lt;/td&gt;
		&lt;td&gt;&lt;p&gt;cell 2&lt;/p&gt;&lt;/td&gt;
	&lt;/tr&gt;
	&lt;tr&gt;
		&lt;td&gt;&lt;p&gt;cell 3, Suspendisse in elit lectus.&lt;/p&gt;&lt;/td&gt;
		&lt;td&gt;&lt;p&gt;cell 4&lt;/p&gt;&lt;/td&gt;
	&lt;/tr&gt;
&lt;/table&gt;
|LiveURL=http://code.webplatform.org/gist/7044174
}}{{Single Example
|Language=CSS
|Description=Here's the CSS for styling the table, above.
|Code=/**
 * Table-layout - Web Platform Docs Examples
 * 
 * An example of table-layout 'auto' and 'fixed'
 * With 'auto', the column stretches to encompass the largest unbreakable element
 * With 'fixed', the column gets the defined width, even though the content might not fit
 *
 * @author	Vivienne van Velzen
 * @see		http://docs.webplatform.org/wiki/css/properties/table-layout 
 */

table {
	border-color: #F00;
	width: 400px;
	table-layout: auto; /* default */
}
table.fixed,
table.fixed2 {
	table-layout: fixed;
}
td {
	border-color: #00F;
}
td.first {
	width: 50px;
}
table.fixed2 td {
	overflow: hidden;
}
p {
	margin: 15px 0 3px 0;
}
td p {
	margin: 3px;
}
|LiveURL=http://code.webplatform.org/gist/7044174
}}
}}
{{Notes_Section
|Notes=* When using 'table-layout: fixed', authors should not omit columns from the first row. If a subsequent row has more columns than the greater of the number determined by the table-column elements and the number determined by the first row, then additional columns may not be rendered.
* If 'table-layout: fixed', any cell that has content that overflows uses the overflow property to determine whether to clip the overflow content.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS2.1, 17.5.2 Table width algorithms: the 'table-layout' property
|URL=http://www.w3.org/TR/CSS2/tables.html#width-layout
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
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
{{See_Also_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}