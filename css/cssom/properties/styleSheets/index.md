{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Cannot finish, Spec is still at Draft level anyway.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Get a list of Style sheets applied to the current document as an ordered collection.}}
{{API_Object_Property
|Property_applies_to=css/cssom/properties
|Read_only=No
|Javascript_data_type=StyleSheetList
|Return_value_description=Get a list of CSS Style Sheets assigned to the current document.
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
Style sheets that are imported using the [[css/atrules/@import|'''@import''']] rule and are contained within the '''style''' object are available through the [[css/cssom/imports|'''imports''']] collection.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Object Model (CSSOM), Section 6.2.3 Extensions to the Document Interface
|URL=http://www.w3.org/TR/cssom/
|Status=W3C Working Draft
}}
}}
{{See_Also_Section
|Manual_links====Related pages===
*<code>[[html/elements/link|link]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/cssom/CSSImportRule|CSSImportRule]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
}}