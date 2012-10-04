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

The index of the newly inserted rule within the media block's rule collection.


}}
{{Topics|DOM}}
{{Notes_Section
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203741 Document Object Model (DOM) Level 2 Style Specification], Section 2.2


===Parameters===
;''bstrRule'' [in]:Type: '''<b>BSTR'''</b>The parsable text that represents the rule. For rule sets, this contains both the selector and the style declaration. For at-rules, this specifies both the at-identifier and the rule content.
;''lIndex'' [in]:Type: '''Integer''' <b/>The index within the media block's rule collection. The rule is inserted immediately before this index. If the specified index is equal to the length of the media block's rule collection, the rule is added to the end of the media block.
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSMediaRule/CSSMediaRule|CSSMediaRule]]</code>
*<code>Reference</code>
*<code>[[css/cssom/styleSheet/cssRules|cssRules]]</code>
*<code>[[css/cssom/CSSMediaRule/deleteRule|deleteRule]]</code>
*<code>[[css/cssom/CSSMediaRule/media|media]]</code>
|Topic_clusters=CSSOM
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}