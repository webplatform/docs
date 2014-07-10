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
|Description=The following '''div''' example renders data in HTML format.
|Code=&lt;div datafld{{=}}"Column2" dataformatas{{=}}"html"&gt;&lt;/div&gt;
}}{{Single Example
|Description=The following '''span''' example renders data in HTML format.
|Code=&lt;span datasrc{{=}}"#bank_acct" datafld{{=}}"balance" dataformatas{{=}}"html"&gt;&lt;/span&gt;
}}{{Single Example
|Description=The following '''textArea''' example renders data in text format.
|Code=&lt;textarea datasrc{{=}}"#customer" datafld{{=}}"address" dataformatas{{=}}"text" rows{{=}}6 COLS{{=}}60&gt;&lt;/textarea&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
As of Windows Internet Explorer 7, the '''DATAFORMATAS''' attribute is no longer supported for the '''input type{{=}}button''' object.
The [[html/attributes/dataFld|'''dataFld''']] property is not available on '''param''' objects; use [[dom/methods/getAttribute|'''getAttribute('dataFld')''']] instead.
Internet Explorer 5.01 or later honors the regional settings for the user's control panel when the '''DATAFORMATAS''' attribute is set to '''localized-text'''. Internet Explorer 5.01 or later performs a locale-dependent type conversion on the native value, instead of using the ''data source object'' to perform the conversion, when binding a textual element such as a '''span''', '''div''', or '''input''' to date, currency, or numeric data. Microsoft Internet Explorer 5 does not provide this feature. To compensate for this limitation, a ''data source object'' can implement '''ISimpleDataConverter''' to participate in the conversion. Neither of these features is supported in earlier versions of Windows Internet Explorer.
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
*<code>button</code>
*<code>div</code>
*<code>input type{{=}}button</code>
*<code>label</code>
*<code>legend</code>
*<code>marquee</code>
*<code>object</code>
*<code>option</code>
*<code>select</code>
*<code>span</code>
*<code>[[html/elements/table|table]]</code>
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