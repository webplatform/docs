{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=examples, compatibility, clean-up of MSDN import to be neutral
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Returns the error message that would be displayed if the user submits the form, or an empty string if no error message.}}
{{API_Object_Property
|Property_applies_to=dom/HTMLInputElement
|Read_only=Yes
|Example_object_name=inputElement
|Return_value_name=validationMessage
|Javascript_data_type=String
|Return_value_description=The error message that would be displayed if the user submits the form, or an empty string if no error message.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=Returns a string containing the standard or custom error message that would be displayed if the user submitted at this time. If no errors are present or the form would validate, an empty string is returned.
The following example has a required field, and if the user types "fun" into it, a custom message is set. Try previewing without anything in the field, then enter values, including the word fun:
'''Note'''  For more  code samples, see [http://go.microsoft.com/fwlink/p/?LinkID{{=}}251128 Form controls part 1] and [http://go.microsoft.com/fwlink/p/?LinkID{{=}}251131 Form controls part 2: validation] on the Windows Internet Explorer sample site.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C HTML5
|URL=http://www.w3.org/TR/html5/
|Status=Working Draft
|Relevant_changes=Section 4
}}{{Related Specification
|Name=WHATWG HTML
|URL=http://www.whatwg.org/specs/web-apps/current-work/multipage
|Status=Living Standard
|Relevant_changes=Section 4
}}
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
*<code>[[dom/HTMLObjectElement|HTMLObjectElement]]</code>
*<code>[[dom/HTMLSelectElement|HTMLSelectElement]]</code>
*<code>[[dom/HTMLInputElement|HTMLInputElement]]</code>
*<code>[[dom/HTMLFieldSetElement|HTMLFieldSetElement]]</code>
*<code>[[dom/HTMLBGSoundElement|HTMLButtonElement]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}