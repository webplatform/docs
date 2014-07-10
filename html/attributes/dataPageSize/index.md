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
|Description=In this example, a text box is bound to the customer_name field supplied by a data source object with an ID of customer. Because the text box is located within a data-bound [[html/elements/table|'''table''']], the text box is repeated to display each of the records in the data source. The '''DATAPAGESIZE''' attribute on the '''table''' limits the display to 10 records.
|Code=&lt;table datasrc{{=}}"#customer" datapagesize{{=}}10&gt;
   &lt;tr&gt;&lt;td&gt;&lt;input type{{=}}texbox datafld{{=}}"customer_name"&gt;&lt;/td&gt;&lt;/tr&gt;
&lt;/table&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The [[dom/methods/firstPage|'''firstPage''']] and [[dom/methods/lastPage|'''lastPage''']] methods are used to navigate directly to the first and last pages of a databound table, respectively. The '''nextPage''' and [[dom/methods/previousPage|'''previousPage''']] methods are used to navigate sequentially through the pages of a databound table.
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
*<code>[[html/elements/table|table]]</code>
*<code>Reference</code>
*<code>[[dom/methods/firstPage|firstPage]]</code>
*<code>[[dom/methods/lastPage|lastPage]]</code>
*<code>nextPage</code>
*<code>[[dom/methods/previousPage|previousPage]]</code>
*<code>Conceptual</code>
*<code>Introduction to Data Binding</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}