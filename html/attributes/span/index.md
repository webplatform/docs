{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info

|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example sets the '''SPAN''' attribute of the '''col''' object to two, which causes the '''col''' to span two columns. The text is right-aligned in these two columns.
|Code=&lt;TABLE BORDER&gt;
&lt;COLGROUP&gt;
&lt;COL SPAN{{=}}2 ALIGN{{=}}RIGHT&gt;
&lt;COL ALIGN{{=}}LEFT&gt;
&lt;TBODY&gt;
&lt;TR&gt;
&lt;TD&gt;This is the first column in the group, and it is 
    right-aligned.&lt;/TD&gt;
&lt;TD&gt;This is the second column in the group, and it is 
    right-aligned.&lt;/TD&gt;
&lt;TD&gt;This is the third column in the group, and it is 
    left-aligned.&lt;/TD&gt;
&lt;/TR&gt;
&lt;/TABLE&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/span.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''span''' property is ignored when set on the '''colGroup''' element and '''colGroup''' contains one or more '''col''' elements. The '''span''' property provides a more convenient way of grouping columns without having to specify '''col''' objects.
|Import_Notes====Syntax===
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
|Manual_sections====Related pages (MSDN)===
*<code>col</code>
*<code>colGroup</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}