{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent, Children and Compatibility information.
|Checked_Out=No
|Content=Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The '''colgroup''' element (&lt;colgroup&gt;) specifies a group of one or more columns in a table for formatting.
This element is useful for applying properties to entire columns, instead of repeating the properties for each cell, for each row.
}}
{{Markup_Element
|DOM_interface=dom/HTMLTableColElement
|Tag_omissions=End tag omissable
|CSS_display=table-column-group
|Content=== HTML Attributes ==
*<code>span</code> = valid non-negative integer

}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
|Description=This example uses the '''COLGROUP''' element to assign specific characteristics to two groups of columns in a table.
|Code=&lt;html&gt;
&lt;body&gt;
&lt;table border{{=}}"2" rules{{=}}"groups"&gt;
    &lt;!-- RULES is set to "groups", which places internal dividing lines around 
table columns defined by COLGROUP. --&gt;
    &lt;colgroup span{{=}}"2" style{{=}}"color: red"&gt;
    &lt;/colgroup&gt;
    &lt;colgroup style{{=}}"color: blue"&gt;
    &lt;/colgroup&gt;
    &lt;tr&gt;
        &lt;td&gt;This column is in the first group.&lt;/td&gt;
        &lt;td&gt;This column is in the first group.&lt;/td&gt;
        &lt;td&gt;This column is in the second group.&lt;/td&gt;
    &lt;/tr&gt;
    &lt;tr&gt;
        &lt;td&gt;This column is in the first group.&lt;/td&gt;
        &lt;td&gt;This column is in the first group.&lt;/td&gt;
        &lt;td&gt;This column is in the second group.&lt;/td&gt;
    &lt;/tr&gt;
&lt;/table&gt;
&lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/colgroupEX1.htm
}}{{Single Example
|Language=
|Description=When '''COL''' elements are nested inside a '''COLGROUP''' element, the attributes of the '''COL''' elements override the attributes of the '''COLGROUP''' element. In this example, the last column has no formatting even though '''COLGROUP''' spans over all three columns. This happens because the [[html/attributes/span|'''SPAN''']] attribute of the nested '''COL''' element overrides the '''SPAN''' attribute of the '''COLGROUP'''.
|Code=&lt;html&gt;
&lt;body&gt;
&lt;table border{{=}}"2"&gt;
    &lt;colgroup span{{=}}"3" style{{=}}"color: green; background: black"&gt;
        &lt;!-- Styling is applied to only the first two columns, instead of all
    three, and the font color is red instead of green. This is consistent
    with the attributes of the COL element. --&gt;
        &lt;col span{{=}}"2" style{{=}}"color: red"&gt;
    &lt;/colgroup&gt;
    &lt;tr&gt;
        &lt;td&gt;This column is in the first group.&lt;/td&gt;
        &lt;td&gt;This column is in the first group.&lt;/td&gt;
        &lt;td&gt;This column is in the second group.&lt;/td&gt;
    &lt;/tr&gt;
    &lt;tr&gt;
        &lt;td&gt;This column is in the first group.&lt;/td&gt;
        &lt;td&gt;This column is in the first group.&lt;/td&gt;
        &lt;td&gt;This column is in the second group.&lt;/td&gt;
    &lt;/tr&gt;
&lt;/table&gt;
&lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/colgroupEX2.htm
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===

Nested '''COL''' elements override '''COLGROUP''' elements.
Use the [[html/attributes/span|'''SPAN''']] attribute to specify the number of table columns that the '''COLGROUP''' defines. This attribute has a default value equal to one.

'''COL''' elements can occur outside of a '''COLGROUP''' element, and these two elements can be used for similar purposes. However, you must use the '''COLGROUP''' element to determine where table internal dividing lines ([[html/attributes/rules|'''rules''']]) should go. This is illustrated in the first example .

You should avoid using the [[html/attributes/span|'''SPAN''']] attribute inside the '''COLGROUP''' element if there are '''COL''' elements nested within it. This is because the '''SPAN''' attribute that belongs to the nested '''COL''' elements will override the attribute that belongs to the '''COLGROUP''' element. This can cause confusing code and possibly unintended results. This behavior is illustrated in the second example.

The [[html/elements/table|'''table''']] object and its associated elements have a separate table object model, which uses different methods than the general object model. For more information on the table object model, see Building Tables Dynamically.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/tabular-data.html#the-colgroup-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/tabular-data.html#the-colgroup-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/tables.html#edef-COLGROUP
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=HTML, Tables
|Manual_links=
|External_links=
|Manual_sections=*<code>col</code>
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