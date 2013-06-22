{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Specifies the placement of a table caption.}}
{{CSS Property
|Initial value=top
|Applies to=Table-caption elements
|Inherited=Yes
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=top
|Description=Positions the caption box above the table box.
}}{{CSS Property Value
|Data Type=bottom
|Description=Positions the caption box below the table box.
}}{{CSS Property Value
|Data Type=inherit
|Description=Takes the same specified value as the property for the element's parent.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example constructs a table with standard HTML elements.
The style rule places the caption above the table.
|Code=&lt;meta http-equiv{{=}}"X-UA-Compatible" content{{=}}"IE{{=}}8" /&gt;
				
&lt;style type{{=}}"text/css"&gt;
caption {
    caption-side:top;
}
&lt;/style&gt;
&lt;table&gt;&lt;tr&gt;&lt;td&gt;A simple table.&lt;/td&gt;&lt;/tr&gt;
&lt;caption&gt;Table caption.&lt;/caption&gt;
&lt;/table&gt;
}}{{Single Example
|Description=This example uses CSS to construct a table using
[[css/properties/display|'''display''']]
attributes. This caption is also placed above its associated table.
|Code=&lt;meta http-equiv{{=}}"X-UA-Compatible" content{{=}}"IE{{=}}8" /&gt;
				
&lt;style type{{=}}"text/css"&gt;
.table {
    display:table;
    border:1px #eee outset;
    border-spacing:2px;
}
.cell {
    display:table-cell;
    border:1px solid black;
}
.caption {
    display:table-caption;
    caption-side:top;
}
&lt;/style&gt;
&lt;div class{{=}}"table"&gt;
&lt;span class{{=}}"cell"&gt;Table content.&lt;/span&gt;
&lt;em class{{=}}"caption"&gt;A caption.&lt;/em&gt;
&lt;/div&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The supported possible values for '''caption-side''' depend on the orientation of the table. Horizontal tables ([[css/properties/writing-mode|'''-ms-writing-mode''']] set to <code>lr-*</code> or <code>rl-*</code>) support the <code>top</code> and <code>bottom</code> values. Vertical tables ('''-ms-writing-mode''' set to <code>tb-*</code> or <code>bt-*</code>) support the <code>left</code> and <code>right</code> values.
Using an unsupported value for this property (for instance, <code>left</code> on a caption for a horizontal table) will cause the caption to appear at the "logical top" of the table. The logical top of a table depends on the writing mode of the text, and is parallel to and immediately precedes the first line of text in a table.
Captions placed to the left or right of the table are not rotated so as to be read vertically. To do this, use the Rotation property of the BasicImage filter (Windows Internet Explorer only).
This style attribute can be applied to any element with a
[[css/properties/display|'''display''']]
style of
'''table-caption'''.
This property requires Internet Explorer to be in
IE8 Standards mode rendering.
|Import_Notes====Syntax===
<code>'''caption-side: '''top '''{{!}}''' bottom</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 17.4.1
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Tables
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/display|display]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}