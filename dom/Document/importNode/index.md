{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=pNodeSource|Data type=IHTMLDOMNode|Description=A reference to the
'''element''' object   that  refers to the node to  move.|Optional=}}
{{Method Parameter|Name=fDeep|Data type=VARIANT_BOOL|Description='''VARIANT_TRUE''' (true)



Child nodes of the node specified by the ''pNodeSource''parameter are also imported.


'''VARIANT_FALSE''' (true)



Child nodes of the node specified by the ''pNodeSource''parameter are not imported.

|Optional=}}
{{Method Parameter|Name=ppNodeDest|Data type=IHTMLDOMNode3|Description=A reference to the
'''element''' object  that refers to the node that has been imported, or a null value if the node cannot be imported.|Optional=}}
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
 

'''IHTMLDOMNode3'''

A reference to the
'''element''' object  that refers to the node that has been imported, or a null value if the node cannot be imported.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following  code example illustrates the '''importNode''' method.
|LiveURL=
|Code=
var oNode {{=}} document.importNode( oXHTMLNode, FALSE );
parent.appendChild( oNode );
}}}}
{{Notes_Section
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182717 Document Object Model (DOM) Level 3 Core Specification], Section 1.4


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}