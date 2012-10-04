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
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

{| class="wikitable"
|-
!Return value
!Description
|-
|S_OK
|The operation completed successfully.
|}
 

Type: '''HRESULT'''

This method can return one of these values.

{| class="wikitable"
|-
!Return value
!Description
|-
|S_OK
|The operation completed successfully.
|}
 


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
If a rule with the given key does not exist, the '''deleteRule''' method does nothing.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkID{{=}}223144 CSS Animations Module Level 3], Section 5


===Parameters===
;''key'' [in]:Type: '''DOMString'''The key that describes the [[css/cssom/CSSKeyframeRule|'''CSSKeyframeRule''']] object to be deleted. The key must resolve to a number between 0 and 1, or the rule is ignored.
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSKeyframesRule|CSSKeyframesRule]]</code>
|Topic_clusters=Animation, CSSOM
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}