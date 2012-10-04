{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=pvarNS|Data type=VARIANT|Description=A '''Variant''' value that contains the name of the desired namespace or a null value if no namespace is desired.|Optional=}}
{{Method Parameter|Name=bstrAttrName|Data type=BSTR|Description=A '''String''' value that contains the name of the desired attribute.|Optional=}}
{{Method Parameter|Name=ppAttribute|Data type=IHTMLDOMAttribute|Description=A reference to an
[[dom/attributes|'''attribute''']]
object that contains the new attribute.|Optional=}}
|Method_applies_to=dom/document
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

{| class="wikitable"
|-
!Return code
!Description
|-
|S_OK
|The operation completed successfully.
|}
 

'''IHTMLDOMAttribute'''

A reference to an
[[dom/attributes|'''attribute''']]
object that contains the new attribute.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
The '''createAttributeNS''' method is supported only for XML documents.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182717 Document Object Model (DOM) Level 3 Core Specification], Section 1.4


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
*<code>[[dom/methods/createAttribute|createAttribute]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}