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
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkID{{=}}223144 CSS Animations Module Level 3], Section 5


===Parameters===
;''rule'' [in]:Type: '''DOMString'''The [[css/cssom/CSSKeyframeRule|'''CSSKeyframeRule''']] object to be inserted, expressed in the same syntax as one entry in the [[css/atrules/@keyframes|'''@keyframes''']] rule. The key, which describes the point at which the rule should be inserted, is included in the rule string. If a rule with the same key already exists in the list, this rule replaces it.
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