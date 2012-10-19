{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Gets a list of CSS rules of a style sheet.}}
{{API_Object_Property
|Property_applies_to=css/cssom/styleSheet
|Read_only=Yes
|Example_object_name=stylesheet
|Return_value_name=rules
|Javascript_data_type=DOM Node
|Return_value_description=Of type CSSRuleList.
A list of CSS rules within a style sheet.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=The list retrieved includes both rule sets (at-rules.
Rules are returned in the same order as they are listed in the parent object. Rules that were dropped during parsing (for instance, because of syntax errors) are not included. However, rules that use a selector or property that Windows Internet Explorer does not recognize are included in the list.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 Style
|URL=http://www.w3.org/TR/2000/REC-DOM-Level-2-Style-20001113/css.html#CSS-CSSMediaRule
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
*<code>[[css/cssom/CSSMediaRule/CSSMediaRule|CSSMediaRule]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}