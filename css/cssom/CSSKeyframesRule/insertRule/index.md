{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs cleanup and elaboration. Usage is unclear and stray extra open bracket being printed by code someplace. defining "HRESULT" or including a link to definition can help provide context to jargon words. Related links can also be condensed. A list of that length can be intimidating.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters=
|Method_applies_to=css/cssom/CSSKeyframesRule
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
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkID{{=}}223144 CSS Animations Module Level 3], Section 5


===Parameters===
;''rule'' [in]:Type: '''DOMString'''The [[css/cssom/CSSKeyframeRule|'''CSSKeyframeRule''']] object to be inserted, expressed in the same syntax as one entry in the [[css/atrules/@keyframes|'''@keyframes''']] rule. The key, which describes the point at which the rule should be inserted, is included in the rule string. If a rule with the same key already exists in the list, this rule replaces it.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Animation, CSSOM
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSKeyframesRule|CSSKeyframesRule]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}