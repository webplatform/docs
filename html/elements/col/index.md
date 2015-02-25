{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent, Children and Compatibility information. Modify DOM Interface information.
|Checked_Out=No
|High-level issues=Data Not Semantic
|Content=Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''col''' element (&lt;col&gt;) specifies  properties for each column within a [[html/elements/colgroup|&lt;colgroup&gt;]] element in a [[html/elements/table|&lt;table&gt;]].}}
{{Markup_Element
|DOM_interface=dom/HTMLTableColElement
|Tag_omissions=No closing tag (self-closing)
|CSS_display=table-column
|Content=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
|Description=This example uses the '''col''' element to specify characteristics for default columns in a table.
|Code=&lt;HTML&gt;
&lt;BODY&gt;
&lt;TABLE BORDER{{=}}"2" RULES{{=}}"groups"&gt;
&lt;!-- RULES is set to "groups", which has no effect in this sample. For this 
attribute to work, you must use COLSPAN to define the groups of columns.--&gt;
    &lt;COL SPAN{{=}}"2" STYLE{{=}}"color:red"&gt;
    &lt;COL STYLE{{=}}"color:blue"&gt;
    &lt;TR&gt;
        &lt;TD&gt;This column is in the first group.&lt;/TD&gt;
        &lt;TD&gt;This column is in the first group.&lt;/TD&gt;
        &lt;TD&gt;This column is in the second group.&lt;/TD&gt;
    &lt;/TR&gt;
    &lt;TR&gt;
        &lt;TD&gt;This column is in the first group.&lt;/TD&gt;
        &lt;TD&gt;This column is in the first group.&lt;/TD&gt;
        &lt;TD&gt;This column is in the second group.&lt;/TD&gt;
    &lt;/TR&gt;
&lt;/TABLE&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
'''COL''' elements can be nested within a '''COLGROUP''' element. If this is done, the nested '''COL''' attributes override the '''COLGROUP''' attributes.
You can use the '''COL''' and '''COLGROUP''' elements for similar purposes. However, you must use the '''COLGROUP''' element to determine where table internal dividing lines ([[html/attributes/rules|'''rules''']]) should go. This is illustrated in the following example.
Use the [[html/attributes/span|'''SPAN''']] attribute to specify the number of table columns that the '''COLGROUP''' defines. This attribute has a default value equal to one.
The [[html/elements/table|'''table''']] object and its associated elements have a separate table object model, which uses different methods than the general object model.  For more information on the table object model, see Building Tables Dynamically.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/tabular-data.html#the-col-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/tabular-data.html#the-col-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/tables.html#edef-COL
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=HTML, Tables
|Manual_links=* [[html/elements/colgroup|colgroup]]
|External_links=
|Manual_sections=
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}