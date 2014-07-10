{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info

|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets or retrieves the source of the data for data binding.}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=In this example, a text box is bound to the customer_name field of a data source object with an ID of "customer." Because the text box is located in a data-bound [[html/elements/table|'''table''']], it is repeated to display each of the records provided by the data source.
|Code=&lt;table datasrc{{=}}"#customer"&gt; 
   &lt;tr&gt;&lt;td&gt;&lt;input type{{=}}"textbox" datafld{{=}}"customer_name"&gt;&lt;td&gt;&lt;tr&gt;
&lt;/table&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The [[html/attributes/dataFld|'''dataFld''']] property is not available on '''param''' objects; use [[dom/methods/getAttribute|'''getAttribute('dataFld')''']] instead.
Tabular and single-valued data consumers use the '''dataSrc''' property to specify a binding. The property takes a string that corresponds to the unique identifier of a data source object (DSO) on the page. The string must be prefixed by a number sign (#).
When the '''dataSrc''' property is applied to a tabular data consumer, the entire data set is repeated by the consuming elements.
When the '''dataSrc''' property is applied to a [[html/elements/table|'''table''']], any contained single-valued consumer objects that specify a [[html/attributes/dataFld|'''dataFld''']] property are repeated for each record in the supplied data set. To complete the binding, the binding agent interrogates the enclosing '''table''' for its data source. A tabular data consumer contained within another tabular data consumer ('''table''') must specify an explicit '''dataSrc'''.
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
*<code>[[html/elements/a|a]]</code>
*<code>applet</code>
*<code>button</code>
*<code>div</code>
*<code>frame</code>
*<code>iframe</code>
*<code>img</code>
*<code>input type{{=}}button</code>
*<code>input type{{=}}checkbox</code>
*<code>input type{{=}}hidden</code>
*<code>input type{{=}}image</code>
*<code>input type{{=}}password</code>
*<code>input type{{=}}radio</code>
*<code>input type{{=}}text</code>
*<code>label</code>
*<code>legend</code>
*<code>marquee</code>
*<code>object</code>
*<code>option</code>
*<code>select</code>
*<code>span</code>
*<code>[[html/elements/table|table]]</code>
*<code>textArea</code>
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