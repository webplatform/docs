{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Adds a new CSS rule to the stylesheet.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=ruleText
|Data type=String
|Description=The at-identifier ("@''rule_name''") and the rule content.
|Optional=No
}}{{Method Parameter
|Name=index
|Data type=Number
|Description=The index within the style sheet's rule list of the rule before which to insert the specified rule. If the specified index equals the length of the style sheet's rule list, the rule will be added to the end of the style sheet.
|Optional=No
}}
|Method_applies_to=css/cssom/styleSheet
|Example_object_name=stylesheet
|Return_value_name=index
|Javascript_data_type=Number
|Return_value_description=The newly inserted rule's index within the style sheet's rule list.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=After the new rule has been inserted, it becomes part of the cascade.
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
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSSOM
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/styleSheet|styleSheet]]</code>
*<code>Reference</code>
*<code>[[css/cssom/styleSheet/cssRules|cssRules]]</code>
*<code>[[css/cssom/styleSheet/deleteRule|deleteRule]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}