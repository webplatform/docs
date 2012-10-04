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
!Return code/value
!Description
|-
|S_OK
|The operation completed successfully.
|-
|DOMException.SYNTAX_ERR
12
|The transformValue string cannot be parsed into an MSCSSMatrix. This occurs when the string is not a valid value for the transform property, or if the string contains relative units.
|}
 

Type: '''HRESULT'''

This method can return one of these values.

{| class="wikitable"
|-
!Return code/value
!Description
|-
|S_OK
|The operation completed successfully.
|-
|DOMException.SYNTAX_ERR
12
|The transformValue string cannot be parsed into an MSCSSMatrix. This occurs when the string is not a valid value for the transform property, or if the string contains relative units.
|}
 


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
Using the '''setMatrixValue''' method and setting the [[css/transforms/MSCSSMatrix|'''MSCSSMatrix''']] attributes individually are the only ways to modify the current matrix. No other method will alter the current matrix.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}223140 CSS Transitions Module Level 3], Section 10.1


===Parameters===
;''transformValue'' [in]:Type: '''DOMString'''A string in the form of an acceptable value for the [[css/transforms/transform|'''transform''']] property in CSS.
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/transforms/MSCSSMatrix|MSCSSMatrix]]</code>
|Topic_clusters=Transforms
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}