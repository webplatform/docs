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
 

DOMString

A string value that corresponds to the matrix. This string value contains matrix(, followed by a comma-and-whitespace-delimited list of matrix values, followed by ).

For a 2-D transform matrix, the matrix value list is ordered [[css/MSCSSMatrix/apis/properties/a|'''a''']], [[css/cssom/MSCSSMatrix/properties/b|'''b''']], [[css/cssom/MSCSSMatrix/properties/c|'''c''']], [[css/cssom/MSCSSMatrix/properties/d|'''d''']], [[css/cssom/MSCSSMatrix/properties/e|'''e''']], [[css/cssom/MSCSSMatrix/properties/f|'''f''']].

For a 3-D transform matrix, the matrix value list is ordered [[css/cssom/MSCSSMatrix/properties/m11|'''m11''']], [[css/cssom/MSCSSMatrix/properties/m21|'''m21''']], [[css/cssom/MSCSSMatrix/properties/m31|'''m31''']], [[css/cssom/MSCSSMatrix/properties/m41|'''m41''']], [[css/cssom/MSCSSMatrix/properties/m12|'''m12''']], [[css/cssom/MSCSSMatrix/properties/m22|'''m22''']], [[css/cssom/MSCSSMatrix/properties/m32|'''m32''']], [[css/cssom/MSCSSMatrix/properties/m42|'''m42''']], [[css/cssom/MSCSSMatrix/properties/m13|'''m13''']], [[css/cssom/MSCSSMatrix/properties/m23|'''m23''']], [[css/cssom/MSCSSMatrix/properties/m33|'''m33''']], [[css/cssom/MSCSSMatrix/properties/m43|'''m43''']], [[css/cssom/MSCSSMatrix/properties/m14|'''m14''']], [[css/cssom/MSCSSMatrix/properties/m24|'''m24''']], [[css/cssom/MSCSSMatrix/properties/m34|'''m34''']], [[css/cssom/MSCSSMatrix/properties/m44|'''m44''']].


}}
{{Topics|DOM}}
{{Notes_Section
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}223140 CSS Transitions Module Level 3], Section 10.1


===Parameters===
;''matrixString'' [out, retval]:Type: '''DOMString'''A string value that corresponds to the matrix. This string value contains <code>matrix(</code>, followed by a comma-and-whitespace-delimited list of matrix values, followed by <code>)</code>.<table><tr><th>Value</th><th>Meaning</th></tr><tr><td width{{=}}"40%"><a id{{=}}"matrix_a__b__c__d__e__f_"/><a id{{=}}"MATRIX_A__B__C__D__E__F_"/><dl><dt>'''matrix(a, b, c, d, e, f)'''</dt></dl></td><td width{{=}}"60%">For a 2-D transform matrix, the matrix value list is ordered [[css/MSCSSMatrix/apis/properties/a|'''a''']], [[css/cssom/MSCSSMatrix/properties/b|'''b''']], [[css/cssom/MSCSSMatrix/properties/c|'''c''']], [[css/cssom/MSCSSMatrix/properties/d|'''d''']], [[css/cssom/MSCSSMatrix/properties/e|'''e''']], [[css/cssom/MSCSSMatrix/properties/f|'''f''']].</td></tr><tr><td width{{=}}"40%"><a id{{=}}"matrix_m11__m21__m31__m41__m12__m22__m32__m42__m13__m23__m33__m43__m14__m24__m34__m44_"/><a id{{=}}"MATRIX_M11__M21__M31__M41__M12__M22__M32__M42__M13__M23__M33__M43__M14__M24__M34__M44_"/><dl><dt>'''matrix(m11, m21, m31, m41, m12, m22, m32, m42, m13, m23, m33, m43, m14, m24, m34, m44)'''</dt></dl></td><td width{{=}}"60%">For a 3-D transform matrix, the matrix value list is ordered [[css/cssom/MSCSSMatrix/properties/m11|'''m11''']], [[css/cssom/MSCSSMatrix/properties/m21|'''m21''']], [[css/cssom/MSCSSMatrix/properties/m31|'''m31''']], [[css/cssom/MSCSSMatrix/properties/m41|'''m41''']], [[css/cssom/MSCSSMatrix/properties/m12|'''m12''']], [[css/cssom/MSCSSMatrix/properties/m22|'''m22''']], [[css/cssom/MSCSSMatrix/properties/m32|'''m32''']], [[css/cssom/MSCSSMatrix/properties/m42|'''m42''']], [[css/cssom/MSCSSMatrix/properties/m13|'''m13''']], [[css/cssom/MSCSSMatrix/properties/m23|'''m23''']], [[css/cssom/MSCSSMatrix/properties/m33|'''m33''']], [[css/cssom/MSCSSMatrix/properties/m43|'''m43''']], [[css/cssom/MSCSSMatrix/properties/m14|'''m14''']], [[css/cssom/MSCSSMatrix/properties/m24|'''m24''']], [[css/cssom/MSCSSMatrix/properties/m34|'''m34''']], [[css/cssom/MSCSSMatrix/properties/m44|'''m44''']].</td></tr></table> 
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