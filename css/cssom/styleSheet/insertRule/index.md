{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters=
|Method_applies_to=
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''Integer'''

The newly inserted rule's index within the style sheet's rule list.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
After the new rule has been inserted, it becomes part of the cascade.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203741 Document Object Model (DOM) Level 2 Style Specification], Section 2.2


===Parameters===
;''bstrRule'' [in]:Type: <b>at-rules, this specifies both the at-identifier ("@''rule_name''") and the rule content.
;''lIndex'' [in]:Type: '''Integer''' <b/>The index within the style sheet's rule list of the rule before which to insert the specified rule. If the specified index equals the length of the style sheet's rule list, the rule will be added to the end of the style sheet.
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/styleSheet|styleSheet]]</code>
*<code>Reference</code>
*<code>[[css/cssom/styleSheet/cssRules|cssRules]]</code>
*<code>[[css/cssom/styleSheet/deleteRule|deleteRule]]</code>
|Topic_clusters=CSSOM
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}