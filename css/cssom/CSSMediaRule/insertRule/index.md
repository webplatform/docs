{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Inserts a new rule to a media block.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=ruleText
|Data type=String
|Description=The parsable text that represents the rule. For rule sets, this contains both the selector and the style declaration. For at-rules, this specifies both the at-identifier and the rule content.
|Optional=No
}}{{Method Parameter
|Name=index
|Data type=Number
|Description=The index within the media block's rule collection. The rule is inserted immediately before this index. If the specified index is equal to the length of the media block's rule collection, the rule is added to the end of the media block.
|Optional=No
}}
|Method_applies_to=css/cssom/CSSMediaRule/CSSMediaRule
|Example_object_name=mediaRule
|Return_value_name=ruleIndex
|Javascript_data_type=Number
|Return_value_description=The index of the newly inserted rule within the media block's rule collection.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203741 Document Object Model (DOM) Level 2 Style Specification], 
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
*<code>[[css/cssom/CSSMediaRule/CSSMediaRule|CSSMediaRule]]</code>
*<code>Reference</code>
*<code>[[css/cssom/styleSheet/cssRules|cssRules]]</code>
*<code>[[css/cssom/CSSMediaRule/deleteRule|deleteRule]]</code>
*<code>[[css/cssom/CSSMediaRule/media|media]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}