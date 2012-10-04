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

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

IHTMLW3CComputedStyle

A [[css/cssom/currentStyle|'''currentStyle''']] object that contains the CSS settings applied to the desired object.

The settings in the ''ppComputedStyle'' object account for all applicable style rules and represent the final values for the various CSS properties applied to the specified object.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
When the ''bstrPseudoElt'' is set to a value other than null, the value is interpreted as a CSS pseudo-element with respect to the object specified in the ''varArgIn'' parameter.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203741 Document Object Model (DOM) Level 2 Style Specification], Section 2.2.1


===Parameters===
;''varArgIn'' [in]:Type: '''<b>IHTMLDOMNode'''</b>The element that contains the desired style settings.
;''bstrPseudoElt'' [in]:Type: '''<b>BSTR'''</b>The name of a CSS pseudo-element or a null value.
;''ppComputedStyle'' [out, retval]:Type: '''IHTMLW3CComputedStyle'''A [[css/cssom/currentStyle|'''currentStyle''']] object that contains the CSS settings applied to the desired object.The settings in the ''ppComputedStyle'' object account for all applicable style rules and represent the final values for the various CSS properties applied to the specified object.
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>window</code>
|Topic_clusters=CSSOM
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}