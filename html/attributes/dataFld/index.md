{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets or retrieves a field of a given data source, as specified by the dataSrc property, to bind to the specified object.}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=In this example, a text box is bound to the flavor field supplied by a data source object with an ID of <code>ice_cream</code>. Because the text box is contained in a table, it is repeated, and all values in the flavor column are displayed.
|Code=&lt;table datasrc{{=}}"#ice_cream"&gt;
   &lt;tr&gt;&lt;td&gt;&lt;input type{{=}}"textbox" datafld{{=}}"flavor"&gt;&lt;/td&gt;&lt;/tr&gt;
&lt;/table&gt;
}}{{Single Example
|Description=In this example, the '''select''' object is bound to the <code>card_type</code> column of a data source control with an ID of <code>order</code>. The value of the field in the data set determines the option that is initially selected. When the user selects a different option from the '''select''', the value of the <code>card_type</code> field in the current record of the data set is updated.
|Code=&lt;select datasrc{{=}}"#order" datafld{{=}}"card_type"&gt;
   &lt;option&gt;Visa
   &lt;option&gt;Mastercard
   &lt;option&gt;American Express
   &lt;option&gt;Diner's Club
   &lt;option&gt;Discover
&lt;/select&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''dataFld''' property is not available on '''param''' objects; use [[dom/methods/getAttribute|'''getAttribute('dataFld')''']] instead.
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
*<code>fieldSet</code>
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
*<code>param</code>
*<code>select</code>
*<code>span</code>
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