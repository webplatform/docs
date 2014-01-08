{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=pAttrNode|Data type=IHTMLDOMAttribute2|Description=The [[dom/attributes|'''attribute''']] to add.|Optional=}}
{{Method Parameter|Name=ppNodeOut|Data type=IHTMLDOMAttribute2|Description=The [[dom/attributes|'''attribute''']] node that the ''pAttrNode'' node replaces, or a null value.|Optional=}}
|Method_applies_to=dom/NamedNodeMap
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
 

'''IHTMLDOMAttribute2'''

The [[dom/attributes|'''attribute''']] node that the ''pAttrNode'' node replaces, or a null value.


}}
{{Topics|DOM}}
{{Notes_Section
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182717 Document Object Model (DOM) Level 3 Core Specification], Section 1.4


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/properties/attribute|attributes]]</code>
*<code>[[dom/methods/setNamedItem|setNamedItem]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}