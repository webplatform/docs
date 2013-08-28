{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The autocomplete attribute specifies whether a form or input field should have autocomplete on or off.}}
{{Markup_Attribute
|Applies_to=html/elements/form
|Property_applies_to=dom/HTMLElement
|Content=When autocomplete is on, the browser automatically complete values based on values that the user has entered before.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''AUTOCOMPLETE''' attribute to disable the AutoComplete feature.
|Code=&lt;INPUT TYPE{{=}}"password" AUTOCOMPLETE{{=}}"off"&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The AutoComplete feature is highlighted in the Using AutoComplete in HTML Forms overview.
When AutoComplete is enabled, suggestions are provided for the [[html/attributes/value (input elements)|'''VALUE''']] of a text field. Suggested values are mapped values based on the [[html/attributes/name|'''NAME''']] attribute or vCard schema specified by the [[html/attributes/vcard_name|'''VCARD_NAME''']] attribute.
If AutoComplete is disabled, values are not stored and suggested values are not presented.
Values in '''input type{{=}}password''' elements can be mapped for AutoComplete; however, the ability to store this information can be disabled in the browser, and the user is prompted for a confirmation before the value is stored.
Information provided by the AutoComplete feature is not exposed to the object model, and is not visible to a Web page until the user selects one of the suggestions as a value for the text field.
This attribute is not supported in HTML Applications (HTAs).
|Import_Notes====Syntax===
===Standards information===
There are no standards that apply here.
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
*<code>input type{{=}}password</code>
*<code>input type{{=}}text</code>
*<code>form</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}