{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs example
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Gets the CSS Rule that imported the style sheet, if any.}}
{{API_Object_Property
|Property_applies_to=css/cssom/styleSheet
|Read_only=Yes
|Example_object_name=stylesheet
|Return_value_name=rule
|Javascript_data_type=DOM Node
|Return_value_description=Of type CSSRule.
Returns a CSSImportRule or null.
|Example_value_name=asd
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=
|Notes=If the style sheet comes from an [[css/atrules/@import|'''@import''']] rule, the '''ownerRule''' property will contain a [[css/cssom/CSSImportRule|'''CSSImportRule''']] object, and the [[css/cssom/styleSheet/ownerNode|'''ownerNode''']] property will be <code>null</code>. If the style sheet comes from a link, the '''ownerRule''' property will be <code>null</code>, and the '''ownerNode''' will contain the node.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 Style
|URL=http://www.w3.org/TR/2000/REC-DOM-Level-2-Style-20001113/css.html
|Status=Recommendation
|Relevant_changes=Section 2.2
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
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/styleSheet|styleSheet]]</code>
*<code>[[css/cssom/styleSheet/cssRules|cssRules]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}