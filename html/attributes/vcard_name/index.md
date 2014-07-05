{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=This attribute is not a part of the W3C standards but IE only.
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
|Description=This example uses the '''VCARD_NAME''' attribute to map the value of the text field to the e-mail address specified by the Profile Assistant.
|Code=&lt;INPUT
TYPE {{=}} text NAME{{=}} "CustomerEmail"
VCARD_NAME {{=}} "vCard.Email"
&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
A vCard is a standards-based way to refer to common personal information about a user.
When a '''VCARD_NAME''' attribute is specified, the AutoComplete box is populated with mapped values from the Profile Assistant and any other submitted values stored for that domain. For example, if a user enters an e-mail address into a text field that exposes a '''VCARD_NAME''' attribute set to <code>vCard.Email</code>, AutoComplete suggests any e-mail information provided in the Profile Assistant. If the user submits a different e-mail address, the new information becomes available on that domain for other text fields with the same '''VCARD_NAME''' value.
If the '''VCARD_NAME''' attribute is not specified, the name of the text field is used to map the submitted information. However, information from the Profile Assistant is not used.
You can disable the AutoComplete feature by specifying <code>no</code> to the [[html/attributes/autocomplete|'''AUTOCOMPLETE''']] attribute.
Even though you can map '''PASSWORD''' values for AutoComplete, the ability to store this information can be disabled. When this occurs, the user is prompted for a confirmation before storing the value.
The object model and the document do not have access to information provided by the AutoComplete feature until the user selects one of the suggestions for the text field.
This property is not supported in HTML Applications.
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
*<code>Using AutoComplete in HTML Forms</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}